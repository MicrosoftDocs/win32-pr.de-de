---
title: Konfigurieren von VBR-Streams
description: Konfigurieren von VBR-Streams
ms.assetid: 83caabb7-b7fa-4b0a-a608-d5a86e4101b8
keywords:
- Streams, Konfigurieren von VBR-Streams
- Streams, Variable Bitrate (VBR)
- variablenbitrate (VBR), Streams
- VBR (Variable Bitrate), Streams
- Streams, iwmpropertyvault-Schnittstelle
- Iwmpropertyvault
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6667dc9cf66932cf8af90da0b0e59ad27860ab3
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103948426"
---
# <a name="configuring-vbr-streams"></a>Konfigurieren von VBR-Streams

Mit der VBR-Codierung (Variable Bitrate) können Sie qualitativ hochwertige Streams für lokale Dateien oder für das herunterladen und Wiedergeben von Daten liefern. Es gibt drei Optionen für VBR: Quality-based (One-Pass), uneingeschränkter (zweipass) und eingeschränkt (Two-Pass). Weitere Informationen zu den Typen der VBR-Codierung finden Sie unter [Variable Bitrate (VBR)-Codierung](variable-bit-rate--vbr--encoding.md).

Sie können die VBR-Codierung in einem Profil konfigurieren, indem Sie Eigenschaften mit der [**iwmpropertyvault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) -Schnittstelle festlegen. In der folgenden Tabelle werden die Eigenschaften zum Konfigurieren der VBR-Codierung beschrieben.



| Eigenschaft                     | BESCHREIBUNG                                                                                       |
|------------------------------|---------------------------------------------------------------------------------------------------|
| **g \_ wszvbrenabled**         | Boolescher Wert. Legen Sie true fest, um die VBR-Codierung zu verwenden.                                                   |
| **g \_ wszvbrquality**         | **DWORD** -Wert. Legen Sie auf die gewünschte Qualitätsstufe (1 bis 100) für die Qualitäts basierte VBR-Codierung fest.      |
| **g \_ wszvbrbitratemax**      | **DWORD** -Wert. Legen Sie die maximale Bitrate in Bits pro Sekunde für die eingeschränkte VBR-Codierung fest.   |
| **g \_ wszvbrbufferwindowmax** | **DWORD** -Wert. Legen Sie auf das maximale Puffer Fenster (in Millisekunden) für die eingeschränkte VBR-Codierung fest. |



 

In den folgenden Abschnitten wird beschrieben, wie die verschiedenen Typen der Variablen Bitrate-Codierung verwendet werden.



| `Section`                                                              | BESCHREIBUNG                                                                                                        |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [So konfigurieren Sie Quality-Based VBR](to-configure-quality-based-vbr.md) | Beschreibt, wie die variablenbitrate-Codierung basierend auf einer statischen Qualitätsstufe verwendet wird.                                   |
| [So konfigurieren Sie einen nicht eingeschränkten VBR](to-configure-unconstrained-vbr.md) | Beschreibt die Verwendung der variablenbitrate-Codierung basierend auf einer durchschnittlichen Zielbitrate ohne einen expliziten Spitzenwert. |
| [So konfigurieren Sie eingeschränkte VBR](to-configure-constrained-vbr.md)     | Beschreibt die Verwendung der variablenbitrate-Codierung basierend auf der durchschnittlichen Bitrate des Ziels und einem expliziten Spitzenwert.     |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Konfigurieren von Streams**](configuring-streams.md)
</dt> </dl>

 

 




