---
description: In dieser Schnellstartanleitung erfahren Sie, wie Sie eine Popupbenachrichtigung von einer Desktop-App auslösen.
title: Senden einer Popupbenachrichtigung vom Desktop
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 1D20ED75-E24A-4e60-91AB-CFCBE902A68E
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbSyntax
ms.openlocfilehash: 79f8f65b18fd6774f318541b15d1649b7c25526f46bf3ab57f02edc4788687c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117858654"
---
# <a name="quickstart-sending-a-toast-notification-from-the-desktop"></a>Schnellstart: Senden einer Popupbenachrichtigung vom Desktop

In dieser Schnellstartanleitung erfahren Sie, wie Sie eine Popupbenachrichtigung von einer Desktop-App auslösen.

## <a name="prerequisites"></a>Voraussetzungen

-   Bibliotheken
    -   C++: Runtime.object.lib
    -   C: \# Windows. Winmd
-   Eine Verknüpfung mit Ihrer App mit einem [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md)muss auf dem Startbildschirm installiert werden. Beachten Sie jedoch, dass sie nicht an die Startbildschirm angeheftet werden muss. Weitere Informationen finden Sie unter [Aktivieren von Desktop-Popupbenachrichtigungen über eine AppUserModelID.](enable-desktop-toast-with-appusermodelid.md)
-   Eine Version von Microsoft Visual Studio, die mindestens Windows 8 unterstützt

## <a name="instructions"></a>Anweisungen

### <a name="1-create-your-toast-content"></a>1. Erstellen Ihres Popupinhalts

> [!Note]  
> Wenn Sie eine Popupvorlage angeben, die ein Bild enthält, beachten Sie, dass Desktop-Apps nur lokale Bilder verwenden können. Webimages werden nicht unterstützt. Außerdem muss der Pfad zur lokalen Bilddatei als absoluter (nicht relativer) Pfad angegeben werden.

 


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



### <a name="2-create-and-attach-the-event-handlers"></a>2. Erstellen und Anfügen der Ereignishandler

Registrieren Sie Handler für die Popupereignisse: Aktiviert, Verworfen und Fehler. Eine Desktop-App muss mindestens das Aktiviert-Ereignis abonnieren, damit sie die erwartete Aktivierung der App vom Popup verarbeiten kann, wenn der Benutzer sie auswählt.


```csharp
toast.Activated += ToastActivated;
toast.Dismissed += ToastDismissed;
toast.Failed += ToastFailed;
```



### <a name="3-send-the-toast"></a>3. Senden des Popups

> [!IMPORTANT]
> Sie müssen die [AppUserModelID](../properties/props-system-appusermodel-id.md) der Verknüpfung Ihrer App bei jedem Aufruf von [**CreateToastNotifier**](/uwp/api/Windows.UI.Notifications.ToastNotificationManager?view=winrt-19041)in den Startbildschirm einfügen. Wenn Sie dies nicht tun, wird Ihr Popup nicht angezeigt.

 


```csharp
ToastNotificationManager.CreateToastNotifier(appID).Show(toast);
```



### <a name="4-handle-the-callbacks"></a>4. Verarbeiten der Rückrufe

Stellen Sie das Fenster Ihrer App in den Vordergrund, wenn sie einen "aktivierten" Rückruf von der Popupbenachrichtigung empfängt. Wenn ein Benutzer ein Popup auswählt, wird erwartet, dass die App mit einer Ansicht gestartet wird, die sich auf den Inhalt dieses Popups bezieht.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Beispiel zum Senden von Toastbenachrichtigungen aus Desktop-Apps](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DesktopToasts)
</dt> <dt>

[Aktivieren von Desktoppopupbenachrichtigungen über eine AppUserModelID](enable-desktop-toast-with-appusermodelid.md)
</dt> <dt>

[Popup-XML-Schema](/uwp/schemas/tiles/toastschema/schema-root)
</dt> <dt>

[Übersicht über Popupbenachrichtigungen](/previous-versions/windows/apps/hh779727(v=win.10))
</dt> <dt>

[Schnellstart: Senden einer Popupbenachrichtigung](/previous-versions/windows/apps/hh465448(v=win.10))
</dt> <dt>

[Schnellstart: Senden einer Popup-Pushbenachrichtigung](/previous-versions/windows/hh761487(v=win.10))
</dt> <dt>

[Richtlinien und Prüfliste für Popupbenachrichtigungen](/windows/uwp/design/shell/tiles-and-notifications/)
</dt> <dt>

[Auswählen und Verwenden einer Popupvorlage](/previous-versions/windows/apps/hh465448(v=win.10))
</dt> <dt>

[Behandeln der Aktivierung über eine Popupbenachrichtigung](/previous-versions/windows/apps/hh761468(v=win.10))
</dt> <dt>

[So entscheiden Sie sich für Popupbenachrichtigungen](/previous-versions/windows/apps/hh781238(v=win.10))
</dt> <dt>

[Auswählen einer Popupvorlage](/previous-versions/windows/apps/hh761494(v=win.10))
</dt> <dt>

[Popupaudiooptionen](/previous-versions/windows/apps/hh761492(v=win.10))
</dt> </dl>

 

 
