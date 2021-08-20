---
title: OverrideEAPCertificateSelection
description: Der Registrierungsschlüssel OverrideEAPCertificateSelection bestimmt, ob der Client das Standardmäßige Smartcard-Zertifikatauswahlverhalten überschreibt und dem Benutzer mehr Zertifikate zur Auswahl bereitstellt.
ms.assetid: 469FECA9-FF2A-46B1-9370-0FF28EF2FB33
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d93efec6968fb27b0d27d88c696101815f0b48c36c100f78092d5b559d4c0f7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118085914"
---
# <a name="overrideeapcertificateselection"></a>OverrideEAPCertificateSelection

Der Registrierungsschlüssel OverrideEAPCertificateSelection bestimmt, ob der Client das Standardmäßige Smartcard-Zertifikatauswahlverhalten überschreibt und dem Benutzer mehr Zertifikate zur Auswahl bereitstellt.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\13
   OverrideEAPCertificateSelection = value
```

## <a name="remarks"></a>Hinweise

Dies ist ein **REG \_ BINARY-Wert.**



| Wert | Beschreibung                                                                                                                                                                                          |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x000 | Überschreiben Sie das Standardverhalten nicht.                                                                                                                                                                |
| 0x001 | Wählen Sie das zuletzt angefügte Zertifikat aus der Smartcard aus.                                                                                                                                            |
| 0x010 | Zeigt alle Zertifikate auf der Benutzeroberfläche für die Zertifikatauswahl auf der Smartcard an.                                                                                                                          |
| 0x100 | Zeigt alle Zertifikate in der Benutzeroberfläche für die Zertifikatauswahl aus der Registrierung an.                                                                                                                            |
| 0x101 | Zeigt alle Zertifikate in der Benutzeroberfläche für die Zertifikatauswahl aus der Registrierung und das zuletzt angefügte Zertifikat von der Smartcard an. Zeigt das zuletzt angefügte Zertifikat von der Smartcard wie ausgewählt an. |
| 0x110 | Zeigt alle Zertifikate in der Benutzeroberfläche für die Zertifikatauswahl aus der Registrierung und der Smartcard an.                                                                                                         |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[EAPHost Registry Einstellungen](eaphost-registry-settings.md)
</dt> </dl>

 

 




