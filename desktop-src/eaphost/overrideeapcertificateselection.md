---
title: Overrideeapcertifi| eselection
description: Der Registrierungsschlüssel overrideeapcertifi| eselection bestimmt, ob der Client das standardmäßige Smartcard-Zertifikat Auswahl Verhalten außer Kraft setzt, und stellt dem Benutzer mehr Zertifikate zur Auswahl bereit.
ms.assetid: 469FECA9-FF2A-46B1-9370-0FF28EF2FB33
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d958eeeffba96e7a060ee4dd3edaf8a9935a15d1
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2019
ms.locfileid: "103857855"
---
# <a name="overrideeapcertificateselection"></a>Overrideeapcertifi| eselection

Der Registrierungsschlüssel overrideeapcertifi| eselection bestimmt, ob der Client das standardmäßige Smartcard-Zertifikat Auswahl Verhalten außer Kraft setzt, und stellt dem Benutzer mehr Zertifikate zur Auswahl bereit.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\13
   OverrideEAPCertificateSelection = value
```

## <a name="remarks"></a>Bemerkungen

Dies ist ein **reg- \_ Binärwert** .



| Wert | BESCHREIBUNG                                                                                                                                                                                          |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x000 | Überschreiben Sie nicht das Standardverhalten.                                                                                                                                                                |
| 0x001 | Wählen Sie das zuletzt angefügte Zertifikat von der Smartcard aus.                                                                                                                                            |
| 0x010 | Zeigt alle Zertifikate auf der Smartcard in der Benutzeroberfläche für die Zertifikat Auswahl an.                                                                                                                          |
| 0x100 | Zeigt alle Zertifikate in der Benutzeroberfläche zur Zertifikat Auswahl aus der Registrierung an.                                                                                                                            |
| 0x101 | Zeigt alle Zertifikate in der Benutzeroberfläche zur Zertifikat Auswahl aus der Registrierung und das zuletzt angefügte Zertifikat von der Smartcard an. Zeigt das zuletzt angefügte Zertifikat von der Smartcard an, wie ausgewählt. |
| 0x110 | Zeigt alle Zertifikate in der Benutzeroberfläche für die Zertifikat Auswahl aus der Registrierung und der Smartcard an.                                                                                                         |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[EAPHost-Registrierungs Einstellungen](eaphost-registry-settings.md)
</dt> </dl>

 

 




