---
title: Aufzählen von Lizenzen im Store
description: Aufzählen von Lizenzen im Store
ms.assetid: 1f380b9e-85e4-4190-a809-65dfd4658b7c
keywords:
- Windows Medienformat-SDK, Aufzählen von Lizenzen
- Windows Medienformat-SDK, Lizenzen
- Windows Medienformat-SDK, lokaler Lizenzspeicher
- Digital Rights Management (DRM), Auflisten von Lizenzen
- DRM (Verwaltung digitaler Rechte),Auflisten von Lizenzen
- Digital Rights Management (DRM), Lizenzen
- DRM (Digital Rights Management), Lizenzen
- Digital Rights Management (DRM), lokaler Lizenzspeicher
- DRM (Digital Rights Management), lokaler Lizenzspeicher
- Erweiterte DRM-Client-APIs, Auflisten von Lizenzen
- Erweiterte Client-APIs, Aufzählen von Lizenzen
- Erweiterte APIs des DRM-Clients, Lizenzen
- Erweiterte Client-APIs, Lizenzen
- Erweiterte DRM-Client-APIs, lokaler Lizenzspeicher
- Erweiterte Client-APIs, lokaler Lizenzspeicher
- licenses,enumerating
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d27913a5a35ce9af1f5a4d6fa3cbae808bc2abe89afd5edb05aa927fe4c39227
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117848196"
---
# <a name="enumerating-licenses-in-the-local-license-store"></a>Aufzählen von Lizenzen im Store

Enumeration ist ein Prozess, bei dem Informationen zu den Lizenzen im lokalen Lizenzspeicher abgerufen werden, indem sie einzeln durchlaufen werden. Sie können eine Lizenzenumeration erstellen, indem Sie [**IWMDRMLicenseManagement::CreateLicenseEnumeration**](iwmdrmlicensemanagement-createlicenseenumeration.md)aufrufen.

Der häufigste Grund für das Aufzählen von Lizenzen im Store ist die Suche nach einer bestimmten Lizenz für die Entschlüsselung einiger Inhalte.

Die [**IWMDRMLicense-Schnittstelle**](iwmdrmlicense.md) dient sowohl als Portal für die einzelnen Lizenzergebnisse als auch als Enumerator. Wenn die Lizenzenumeration erstellt wird, wird die erste Lizenz in der Liste in die **IWMDRMLicense-Schnittstelle** geladen. Mit den meisten **IWMDRMLicense-Methoden** können Sie Informationen zur Lizenz abrufen oder Objekte zum Verschlüsseln oder Entschlüsseln von Inhalten basierend auf der Lizenz erstellen. Es gibt jedoch zwei Methoden, die die Enumeration steuern: [**GetNext**](iwmdrmlicense-getnext.md) und [**ResetEnumeration**](iwmdrmlicense-resetenumeration.md). **GetNext** lädt die nächste Lizenz in der Liste in die Schnittstelle. **ResetEnumeration** gibt die Enumeration in den Zustand zurück, in dem sie sich bei der ersten Erstellung befand. Wenn die Enumeration zurückgesetzt wird, wird die erste Lizenz in der Liste wieder in die **IWMDRMLicense-Schnittstelle** geladen.

Wenn Sie die letzte Lizenz in der Liste erreicht haben, gibt der nächste Aufruf von **GetNext** ERROR \_ NO MORE ITEMS \_ \_ zurück.

Wenn Ihre Anwendung eine Aktion mit dem Inhalt ausführt, der von DRM abgedeckt wird, sollten Sie die Lizenzen im lokalen Lizenzspeicher auf die Rechte und andere einschränkende Faktoren überprüfen, z. B. auf Ausgabeschutzebenen (Output Protection Levels, OPLs).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Abrufen von Informationen aus Lizenzen im Store**](getting-information-from-licenses-in-the-local-license-store.md)
</dt> </dl>

 

 




