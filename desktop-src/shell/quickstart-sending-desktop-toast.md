---
description: In dieser Schnellstartanleitung wird veranschaulicht, wie eine Popup Benachrichtigung aus einer Desktop-App erhoben wird.
title: Senden einer Popupbenachrichtigung vom Desktop
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 1D20ED75-E24A-4e60-91AB-CFCBE902A68E
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbSyntax
ms.openlocfilehash: 36f9da25c20d99da74be30046fc5f9f4789dfd73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866148"
---
# <a name="quickstart-sending-a-toast-notification-from-the-desktop"></a>Schnellstart: Senden einer Popup Benachrichtigung vom Desktop

In dieser Schnellstartanleitung wird veranschaulicht, wie eine Popup Benachrichtigung aus einer Desktop-App erhoben wird.

## <a name="prerequisites"></a>Voraussetzungen

-   Bibliotheken
    -   C++: Runtime. Object. lib
    -   C \# : Windows. winmd
-   Auf dem Start Bildschirm muss eine Verknüpfung mit der APP mit [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md)installiert sein. Beachten Sie jedoch, dass es nicht an den Start Bildschirm angeheftet werden muss. Weitere Informationen finden Sie unter Aktivieren von desktoppopup [-Benachrichtigungen über eine appusermodelid](enable-desktop-toast-with-appusermodelid.md).
-   Eine Version von Microsoft Visual Studio, die mindestens Windows 8 unterstützt.

## <a name="instructions"></a>Instructions

### <a name="1-create-your-toast-content"></a>1. Erstellen Sie den Popup Inhalt.

> [!Note]  
> Beachten Sie, dass Desktop-Apps nur lokale Images verwenden können, wenn Sie eine Popup Vorlage angeben, die ein Bild enthält. webimages werden nicht unterstützt. Außerdem muss der Pfad zur lokalen Bilddatei als absoluter (nicht relativer) Pfad angegeben werden.

 


```csharp
// Get a toast XML template
XmlDocument toastXml = ToastNotificationManager.GetTemplateContent(ToastTemplateType.ToastImageAndText04);

// Fill in the text elements
XmlNodeList stringElements = toastXml.GetElementsByTagName("text");
for (int i = 0; i < stringElements.Length; i++)
{
    stringElements[i].AppendChild(toastXml.CreateTextNode("Line " + i));
}

// Specify the absolute path to an image
String imagePath = "file:///" + Path.GetFullPath("toastImageAndText.png");
XmlNodeList imageElements = toastXml.GetElementsByTagName("image");

ToastNotification toast = new ToastNotification(toastXml);
```



### <a name="2-create-and-attach-the-event-handlers"></a>2. erstellen und Anfügen von Ereignis Handlern

Registrieren von Handlern für die Popup Ereignisse: aktiviert, verworfen und fehlerhaft. Eine Desktop-App muss das aktivierte Ereignis zumindest abonnieren, damit Sie die erwartete Aktivierung der APP vom Toast aus verarbeiten kann, wenn der Benutzer Sie auswählt.


```csharp
toast.Activated += ToastActivated;
toast.Dismissed += ToastDismissed;
toast.Failed += ToastFailed;
```



### <a name="3-send-the-toast"></a>3. den Toast senden

> [!IMPORTANT]
> Sie müssen die [appusermodelid](../properties/props-system-appusermodel-id.md) der Verknüpfung ihrer App auf dem Start Bildschirm jedes Mal einschließen, wenn Sie " [**foratetoastnotifier**](/uwp/api/Windows.UI.Notifications.ToastNotificationManager?view=winrt-19041)" aufrufen. Wenn Sie dies nicht tun, wird der Toast nicht angezeigt.

 


```csharp
ToastNotificationManager.CreateToastNotifier(appID).Show(toast);
```



### <a name="4-handle-the-callbacks"></a>4. behandeln Sie die Rückrufe.

Bringen Sie das Fenster ihrer app in den Vordergrund, wenn ein "aktivierter" Rückruf von der Popup Benachrichtigung empfangen wird. Wenn ein Benutzer einen Toast auswählt, wird erwartet, dass die app in einer Ansicht mit dem Inhalt dieses Popups gestartet wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Beispiel zum Senden von Toastbenachrichtigungen aus Desktop-Apps](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DesktopToasts)
</dt> <dt>

[Aktivieren von Desktoppopupbenachrichtigungen über eine AppUserModelID](enable-desktop-toast-with-appusermodelid.md)
</dt> <dt>

[Popup-XML-Schema](/uwp/schemas/tiles/toastschema/schema-root)
</dt> <dt>

[Übersicht über Popup Benachrichtigungen](/previous-versions/windows/apps/hh779727(v=win.10))
</dt> <dt>

[Schnellstart: Senden einer Popup Benachrichtigung](/previous-versions/windows/apps/hh465448(v=win.10))
</dt> <dt>

[Schnellstart: Senden einer Popup-Pushbenachrichtigung](/previous-versions/windows/hh761487(v=win.10))
</dt> <dt>

[Richtlinien und Prüfliste für Popup Benachrichtigungen](/windows/uwp/design/shell/tiles-and-notifications/)
</dt> <dt>

[Auswählen und Verwenden einer Popup Vorlage](/previous-versions/windows/apps/hh465448(v=win.10))
</dt> <dt>

[Behandeln der Aktivierung über eine Popup Benachrichtigung](/previous-versions/windows/apps/hh761468(v=win.10))
</dt> <dt>

[Abonnieren von Popup Benachrichtigungen](/previous-versions/windows/apps/hh781238(v=win.10))
</dt> <dt>

[Auswählen einer Popup Vorlage](/previous-versions/windows/apps/hh761494(v=win.10))
</dt> <dt>

[Popup-Audiooptionen](/previous-versions/windows/apps/hh761492(v=win.10))
</dt> </dl>

 

 
