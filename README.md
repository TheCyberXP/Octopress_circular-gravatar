#Introduction

Plugin to display your Gravatar avatar with a circular style in the sidebar of your Octopress site.

Live example at <a href="http://www.waelammar.com">http://www.waelammar.com</a>

I used the <a href="https://github.com/joet3ch/gravatar-octopress">official Gravatar Octopress plugin</a> developed by **joet3ch** then I added some *CSS* to get the circular and central effect.

##Installation:

1. Copy 'gravatar.html' to your '_includes/custom/asides' directory.
2. Copy 'gravatar.rb' to your 'plugins' directory.
3. Update your '_config.yml' file to include a 'gravatar_email' variable. Example below which is also in the provided _config.yml file:

        # Gravatar  
        gravatar_email: youraddress@example.com

4. Add 'gravatar.html' to your default_asides variable in the '_config.yml' settings file. Example:

        default_asides: [custom/asides/gravatar.html, custom/asides/about.html, asides/twitter.html, asides/recent_posts.html]
        
##Customize Image Size:

You can customize the size of the image in the gravatar.html file:

        width: 100px;
        height: 100px;
        background: url({% gravatar_image 100 %}) no-repeat;

##Remove the center effect:

You can remove the center effect in the gravatar.html file by deleting line 12 and 13:

            display: block;
            margin: 0 auto;
