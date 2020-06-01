# FlexlayoutTest

### Description
Trying to create a kind of toast of android, I used a flexlayout inside the stacklayout to control then height of then content. Using wrap="wrap" or NoWrap works but, when config with Reverse then content isn't renderer. 
Removing the stacklayout then content is rendered but the height is automatically set to whole screen.

### Steps to Reproduce

1. Create a screen with the following code 
```xaml
    <Frame Padding="10"
           CornerRadius="10"
           Margin="10"
           BackgroundColor="Gray"
           VerticalOptions="End"
           HorizontalOptions="Center"
           HasShadow="False">
        <StackLayout >
            <FlexLayout Direction="Row"
                        Wrap="Wrap"
                        JustifyContent="SpaceBetween">
                <Label Text="Teste Label"
                       TextColor="Green"
                       BackgroundColor="LightGreen"/>
                <Label x:Name="xamarin"
                       Margin="0,5"
                       Text="Welcome to Xamarin.Forms!!!!!!"
                       TextColor="Blue"
                       BackgroundColor="LightBlue"
                       HorizontalOptions="EndAndExpand"
                       VerticalOptions="CenterAndExpand" />
            </FlexLayout>
        </StackLayout>
    </Frame>
```

2. Change the property **Wrap** to Reverse

```xaml
    <Frame Padding="10"
           CornerRadius="10"
           Margin="10"
           BackgroundColor="Gray"
           VerticalOptions="End"
           HorizontalOptions="Center"
           HasShadow="False">
        <StackLayout >
            <FlexLayout Direction="Row"
                        Wrap="Reverse"
                        JustifyContent="SpaceBetween">
                <Label Text="Teste Label"
                       TextColor="Green"
                       BackgroundColor="LightGreen"/>
                <Label x:Name="xamarin"
                       Margin="0,5"
                       Text="Welcome to Xamarin.Forms!!!!!!"
                       TextColor="Blue"
                       BackgroundColor="LightBlue"
                       HorizontalOptions="EndAndExpand"
                       VerticalOptions="CenterAndExpand" />
            </FlexLayout>
        </StackLayout>
    </Frame>
```

### Expected Behavior
<img width="330" alt="Expected Behavior" src="https://user-images.githubusercontent.com/9166406/83368504-60542700-a38f-11ea-8d19-c6cbda9a0246.png">

### Actual Behavior
Screen using flexlayout with Wrap="Reverse" inside Stacklayout
<img width="330" alt="Actual Behavior" src="https://user-images.githubusercontent.com/9166406/83368555-9c878780-a38f-11ea-9e6b-a9207d033ca4.png">

Screen using flexlayout with Wrap="Reverse" without Stacklayout
<img width="330" alt="Without Stacklayout" src="https://user-images.githubusercontent.com/9166406/83369274-2df7f900-a392-11ea-9f28-98ec1e35ebc5.png">


### Basic Information

- Version with issue: 4.1 to 4.6
- IDE: Visual Studio for Mac 
- Platform Target Frameworks: <!-- All that apply -->
  - iOS:  13.3
  - Android: 9.0
- Android Support Library Version: 28.0.0.1
- Xamarin: 4.6.0.800

### Reproduction Link

https://github.com/feokuma/FlexlayoutTest

### Workaround

