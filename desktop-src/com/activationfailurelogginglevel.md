---
title: Activationfailurelogginglevel
description: Legt den ausführlichkeits Grad von Ereignisprotokoll Einträgen zu fehlgeschlagenen Anforderungen für das Starten und Aktivieren von Komponenten fest.
ms.assetid: c3981621-5826-405c-8962-edfa9c783c2d
keywords:
- Registrierungs Wert "activationfailurelogginglevel" com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfdd834be35a59dd5d8e207cd679dae68043d70c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388752"
---
# <a name="activationfailurelogginglevel"></a>Activationfailurelogginglevel

Legt den ausführlichkeits Grad von Ereignisprotokoll Einträgen zu fehlgeschlagenen Anforderungen für das Starten und Aktivieren von Komponenten fest.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   ActivationFailureLoggingLevel = value
```

## <a name="remarks"></a>Bemerkungen

Dies ist ein **reg \_ DWORD** -Wert.



| Wert | BESCHREIBUNG                                                                                                                                                                                                       |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Verwenden der freigegebenen Protokollierung. Standardmäßig protokollieren Sie Fehler, Clients können dieses Verhalten jedoch außer Kraft setzen, indem Sie \_ \_ \_ in [**cokreateinstanceex**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex)das CLSCTX No Failure Log angeben. Dies ist der Standardwert. |
| 1     | Alle Fehler unabhängig vom angegebenen Client protokollieren.                                                                                                                                                      |
| 2     | Protokollieren Sie niemals Fehler, unabhängig vom angegebenen Client.                                                                                                                                                       |



 

Wenn Sie eine Anwendung zum Steuern der Ereignisprotokollierung benötigen, empfiehlt es sich, diesen Wert auf 0 festzulegen und den Client Code zu schreiben, um ihn bei Bedarf zu überschreiben. Es wird dringend empfohlen, den Wert nicht auf 2 festzulegen. Wenn die Ereignisprotokollierung deaktiviert ist, ist es schwieriger, Probleme zu diagnostizieren. Bei Fehlern in Bezug auf Computer Einschränkungen, bei denen com keine CLSCTX-Bits hat, behandelt com den Wert 0 als 1.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Festlegen der Sicherheit für COM-Anwendungen](setting-security-for-com-applications.md)
</dt> </dl>

 

 




