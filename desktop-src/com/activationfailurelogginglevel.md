---
title: ActivationFailureLoggingLevel
description: Legt die Ausführlichkeit von Ereignisprotokolleinträgen zu fehlgeschlagenen Anforderungen für den Komponentenstart und die Aktivierung fest.
ms.assetid: c3981621-5826-405c-8962-edfa9c783c2d
keywords:
- ActivationFailureLoggingLevel-Registrierungswert COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a51d0f92dbf1b54d572de44e750fba20ca39954ced57b6276ecdc4b8c4e07960
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119855100"
---
# <a name="activationfailurelogginglevel"></a>ActivationFailureLoggingLevel

Legt die Ausführlichkeit von Ereignisprotokolleinträgen zu fehlgeschlagenen Anforderungen für den Komponentenstart und die Aktivierung fest.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   ActivationFailureLoggingLevel = value
```

## <a name="remarks"></a>Hinweise

Dies ist ein **REG \_ DWORD-Wert.**



| Wert | Beschreibung                                                                                                                                                                                                       |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Verwenden Sie die diskrete Protokollierung. Protokollieren Sie Standardmäßig Fehler, aber Clients können dieses Verhalten überschreiben, indem sie CLSCTX \_ NO FAILURE LOG in \_ \_ [**CoCreateInstanceEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex)angeben. Dies ist der Standardwert. |
| 1     | Protokollieren Sie immer alle Fehler, unabhängig davon, was der Client angegeben hat.                                                                                                                                                      |
| 2     | Protokollieren Sie niemals Fehler, unabhängig davon, was der Client angegeben hat.                                                                                                                                                       |



 

Wenn Sie eine Anwendung zum Steuern der Ereignisprotokollierung benötigen, wird empfohlen, diesen Wert auf 0 festzulegen und den Clientcode zu schreiben, um ihn bei Bedarf zu überschreiben. Es wird dringend empfohlen, den Wert nicht auf 2 festzulegen. Wenn die Ereignisprotokollierung deaktiviert ist, ist es schwieriger, Probleme zu diagnostizieren. Bei Berechtigungsfehlern bei Computereinschränkungen, bei denen COM nicht über CLSCTX-Bits verfügt, behandelt COM den Wert 0 als 1.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Festlegen der Sicherheit für COM-Anwendungen](setting-security-for-com-applications.md)
</dt> </dl>

 

 




