---
title: Rechtekonstanten
description: Rechtekonstanten
ms.assetid: fb20dc57-25da-4613-a324-e081ba87df73
keywords:
- Windows Medienformat-SDK, Konstanten
- Digital Rights Management (DRM), Konstanten
- DRM (Digital Rights Management), Konstanten
- Erweiterte DRM-Client-APIs, Konstanten
- Erweiterte Client-APIs, Konstanten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 088c3130551a6798900ea77cc3628cb784ff7c70b418795157b203ab2f71b64e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110140"
---
# <a name="rights-constants"></a>Rechtekonstanten

Die in der folgenden Tabelle aufgeführten Konstanten werden verwendet, um DRM-Aktionen zu identifizieren und Listen von Aktionen zu erstellen.



| Konstante                                        | Beschreibung                                                                                                                                                                                                                                                    |
|-------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| g \_ wszWMDRM \_ ACTIONLIST \_ TAG                    | Definiert den XML-Elementnamen für eine Aktionsliste.                                                                                                                                                                                                               |
| g \_ wszWMDRM \_ ACTION \_ TAG                        | Definiert den XML-Elementnamen für einen Eintrag in einer Aktionsliste.                                                                                                                                                                                                   |
| g \_ wszWMDRM \_ RIGHT \_ PLAYBACK                    | Definiert die Zeichenfolge für das Recht zum Wiedergeben von Inhalten.                                                                                                                                                                                                              |
| g \_ wszWMDRM \_ RIGHT \_ COPY                        | Definiert die Zeichenfolge für das Recht zum Kopieren von Inhalt.                                                                                                                                                                                                              |
| g \_ wszWMDRM \_ RIGHT PLAYLIST \_ \_ BURN              | Definiert die Zeichenfolge für das Recht, Inhalt als Teil einer Wiedergabeliste auf CD zu verketten.                                                                                                                                                                                  |
| g \_ wszWMDRM \_ RIGHT CREATE THUMBNAIL \_ \_ \_ IMAGE    | Definiert die Zeichenfolge für die Rechte, um ein Miniaturbild aus Videoinhalten zu erstellen.                                                                                                                                                                               |
| g \_ wszWMDRM \_ RIGHT COPY TO \_ \_ \_ CD                | Definiert die Zeichenfolge für das Recht, Inhalt auf eine CD zu kopieren. Neue Lizenzen sollten dieses Recht nicht verwenden. Stattdessen sollten alle Rechte, die die Berechtigung zum Kopieren von Inhalten erteilen, durch das Kopierrecht und das Wiedergabelisten-Burn-Recht abgedeckt werden.                                     |
| g \_ wszWMDRM \_ RIGHT COPY TO \_ \_ \_ SDMI \_ DEVICE      | Definiert die Zeichenfolge für das Recht, Inhalte auf ein Gerät zu kopieren, das der Secure Digital Musik Initiative (SDMI) entspricht. Neue Lizenzen sollten dieses Recht nicht verwenden. Stattdessen sollten alle Rechte, die die Berechtigung zum Kopieren von Inhalten erteilen, durch das Kopierrecht abgedeckt werden. |
| g \_ wszWMDRM \_ RIGHT COPY TO NON \_ \_ \_ \_ SDMI \_ DEVICE | Definiert die Zeichenfolge für das Recht, auf ein Gerät zu kopieren, das nicht der Secure Digital Musik Initiative (SDMI) entspricht. Neue Lizenzen sollten dieses Recht nicht verwenden. Stattdessen sollten alle Rechte, die die Berechtigung zum Kopieren von Inhalten erteilen, durch das Kopierrecht abgedeckt werden. |
| g \_ wszWMDRM \_ RIGHT \_ BACKUP                      | Definiert die Zeichenfolge für das Recht zum Sichern der Lizenz.                                                                                                                                                                                                        |
| g \_ wszWMDRM \_ RIGHT COLLABORATIVE \_ \_ PLAY         | Definiert die Zeichenfolge für das Recht zum Wiedergeben von Inhalten über ein Netzwerk als Teil einer freigegebenen Wiedergabeliste.                                                                                                                                                                  |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Konstanten**](constants.md)
</dt> </dl>

 

 




