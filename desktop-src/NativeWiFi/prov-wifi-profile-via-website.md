---
title: Bereitstellen eines WLAN-Profils über eine Website
description: Ermöglichen Sie Ihren Benutzern, ein Profil von einer Website herunterzuladen und bereitzustellen.
ms.topic: article
ms.date: 01/22/2020
ms.openlocfilehash: e34c83fbee100316256293e27eac96dae685c37d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103949088"
---
# <a name="provision-a-wi-fi-profile-via-a-website"></a>Bereitstellen eines WLAN-Profils über eine Website

Der in diesem Thema beschriebene Workflow wurde in Windows 10, Version 2004, eingeführt. In diesem Thema wird gezeigt, wie Sie eine Website so konfigurieren, dass ein Benutzer ein Profil für ein passpoint-Netzwerk (oder für ein normales Netzwerk) bereitstellen kann, bevor es in den Bereich der entsprechenden Wi-Fi Zugriffspunkte verschoben wird. Ein Beispielszenario ist, dass ein Benutzer, der möglicherweise plant, einen Flughafen oder eine Konferenz zum ersten Mal zu besuchen und sich vorab vorbereiten möchte, indem er ein Profil zu Hause herunterlädt und bereitstellt.

Als Entwickler aktivieren Sie den Workflow, indem Sie ein XML-Profil bereitstellen und eine Website konfigurieren. Ihre Benutzer können dann ein Wi-Fi Profil bereitstellen, indem Sie es über einen Webbrowser von Ihrer Website herunterladen. Auf dem Gerät des Benutzers wird das Wi-Fi Profil mithilfe der URI-Aktivierung und der Windows- **Einstellungs** -App bereitgestellt.

Dieser Workflow ersetzt den Mechanismus in Internet Explorer für die Bereitstellung Wi-Fi Profile, die von Microsoft-spezifischen JavaScript-APIs abhängig sind. Es wird erwartet, dass dieser neue Workflow mit allen wichtigen Browsern funktioniert.

## <a name="the-workflow-in-more-detail"></a>Der Workflow ist ausführlicher.

Sie können diesen Workflow über einen Hyperlink aktivieren, der als Argument den Download-URI des XML-Bereitstellungs Dokuments enthält.

```xml
ms-settings:wifi-provisioning?uri={download_uri}
```

Das folgende HTML-Markup enthält z. b. einen Link zum Installieren der Profile, die in einem hypothetischen Dokument gefunden werden `http://contoso.com/ProvisioningDoc.xml` .

```html
<a href="ms-settings:wifi-provisioning?uri=http://contoso.com/ProvisioningDoc.xml">Install</a>
```

Der XML-Code muss dem Bereitstellungs Schema entsprechen (siehe [Konto Bereitstellung](/windows-hardware/drivers/mobilebroadband/account-provisioning)). Der XML-Code muss auch ein oder mehrere [wlanprofile](./wlan-profileschema-wlanprofile-element.md)-   Elemente enthalten.Jedes Profil wird im Dialogfeld **Hinzufügen** angezeigt, das weiter unten beschrieben wird.

Wenn der Benutzer auf den HTML-Link klickt, wird der Installations Workflow in der App " **Einstellungen** " aufgerufen. Ihr Bereitstellungs-XML-Dokument wird von der App " **Einstellungen** " heruntergeladen. Nach dem herunterladen werden Informationen zu den Profilen, der Signatur und dem Signatur Geber angezeigt (sofern das Dokument dem Schema folgt).

![Die app "Einstellungen"](images/install-dialog.png)

Die Schaltfläche **Hinzufügen** im Dialogfeld in der APP **Einstellungen** ist nur aktiviert, wenn die Bereitstellungs Datei signiert und vertrauenswürdig ist.

## <a name="in-your-web-page-determine-whether-this-workflow-is-supported"></a>Legen Sie auf der Webseite fest, ob dieser Workflow unterstützt wird.

Es gibt keine Möglichkeit in JavaScript, die genaue Buildversion von Windows zu ermitteln. Wenn Ihr Benutzer jedoch den Microsoft Edge-Webbrowser verwendet, können Sie die Version von Edge ermitteln, indem Sie den Wert des-HTTP- `User-agent` Headers überprüfen. Wenn die Version größer oder gleich ist `18.nnnnn` , wird der Workflow unterstützt.

## <a name="related-topics"></a>Zugehörige Themen

* [Konto Bereitstellung](/windows-hardware/drivers/mobilebroadband/account-provisioning)
* [Wlanprofile-Element](./wlan-profileschema-wlanprofile-element.md)