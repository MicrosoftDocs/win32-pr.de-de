---
description: Veranschaulicht, wie die Shell \_ NotifyIcon-und Shell \_ notifyikongetrect-APIs zum Anzeigen eines Benachrichtigungs Symbols verwendet werden.
title: NotificationIcon (Beispiel)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 9F31DB2D-4B12-4f65-AC91-25B4B5B1CB46
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 1569d162aef358130910081bee80354cb64f690d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104979833"
---
# <a name="notificationicon-sample"></a>NotificationIcon (Beispiel)

Veranschaulicht, wie die [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) -und [**Shell \_ notifyikongetrect**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect) -APIs zum Anzeigen eines Benachrichtigungs Symbols verwendet werden.

Dieses Thema enthält folgende Abschnitte:

-   [Beschreibung](#description)
-   [Anforderungen](#requirements)
-   [Herunterladen des Beispiels](#downloading-the-sample)
-   [Beispiel zum Aufbau](#building-the-sample)
-   [Ausführen des Beispiels](#running-the-sample)

## <a name="description"></a>BESCHREIBUNG

Zusätzlich zur Verwendung von [**Shell \_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) und [**Shell \_ notifyikongetrect**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect) zum Anzeigen eines Benachrichtigungs Symbols wird in diesem Beispiel auch veranschaulicht, wie Sie ein umfangreiches Flyout-Fenster, ein Kontextmenü und eine Sprechblasen Benachrichtigung anzeigen.

> [!Note]  
> [**Shell \_ Notisyitrect**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect) ist nur unter Windows 7 und höheren Versionen verfügbar.

 

## <a name="requirements"></a>Requirements (Anforderungen)



| Produkt                                | Minimale Produkt Version |
|----------------------------------------|-------------------------|
| Windows                                | Windows 7               |
| Windows Software Development Kit (SDK) | 7.0                     |



 

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

| Standort      | Pfad-URL                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Notificationicon-Beispiel](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/NotificationIcon) |

## <a name="building-the-sample"></a>Erstellen des Beispiels

So erstellen Sie das Beispiel von der Eingabeaufforderung aus:

1.  Öffnen Sie das Eingabe Aufforderungs Fenster, und navigieren Sie zum Projektverzeichnis **notificationicon** .
2.  Geben Sie `msbuild NotificationIcon.sln` ein.

So erstellen Sie das Beispiel mithilfe Microsoft Visual Studio (bevorzugt):

1.  Öffnen Sie Windows-Explorer, und navigieren Sie zum Projektverzeichnis **notificationicon** .
2.  Doppelklicken Sie auf das Symbol für die Datei notificationicon. sln, um das Projekt in Visual Studio zu öffnen.
3.  Wählen Sie im Menü **Erstellen** die Option Projekt Mappe **Erstellen** aus.

## <a name="running-the-sample"></a>Ausführen des Beispiels

1.  Navigieren Sie mithilfe der Eingabeaufforderung oder Windows-Explorer zu dem Verzeichnis, das die neue ausführbare Datei enthält.
2.  Geben Sie in der Befehlszeile ein `NotificationIcon.exe` . Alternativ können Sie in Windows-Explorer auf das Symbol für NotificationIcon.exe doppelklicken.

> [!Note]  
> Benachrichtigungs Symbole, die mit einer GUID angegeben werden, werden vor Spoofing geschützt, indem überprüft wird, ob Sie nur von einer einzelnen Anwendung registriert werden. Diese Registrierung wird ausgeführt, wenn Sie Shell \_ NotifyIcon (NIM \_ Add,...) zum ersten Mal aufrufen und der vollständige Pfadname der aufrufenden Anwendung gespeichert wird. Wenn Sie die Binärdatei später an einen anderen Speicherort verschieben, lässt das System nicht zu, dass das Symbol erneut hinzugefügt wird. Weitere Informationen finden Sie in der [**Shell \_ notityicon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) .

 

 

 



