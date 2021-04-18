---
description: Beschreibt zwei Arten von Datenträger Kontingent Limits und wie die Datenträger Kontingent Limits gemessen werden.
ms.assetid: 6595d5e0-eb97-437e-abd2-3a04faefde7d
title: Limits für Datenträger Kontingente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f51fff88bcb29d12c52387267c5e910ba36fa15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358544"
---
# <a name="disk-quota-limits"></a>Limits für Datenträger Kontingente

Der Speicherplatz, den die einzelnen Dateien verwenden, wird direkt dem Benutzer in Rechnung gestellt, der die Datei besitzt. Der Besitzer einer Datei wird durch die Sicherheits-ID (Security Identifier, SID) in den Sicherheitsinformationen für die Datei identifiziert. Der Gesamt Speicherplatz, der einem Benutzer in Rechnung gestellt wird, ist die Summe der Länge aller Datenströme. Das heißt, dass Eigenschaften Satz-Streams und residente Benutzerdaten Ströme das Kontingent des Benutzers beeinflussen.

Das Kontingent wird für erneute Analyse Punkte, Sicherheits Deskriptoren oder andere Metadaten, die den Dateien zugeordnet sind, nicht in Rechnung gestellt. Das komprimieren oder Dekomprimieren von Dateien wirkt sich nicht auf den für die Dateien gemeldeten Speicherplatz aus. Daher können Kontingent Einstellungen auf einem Volume mit Einstellungen auf einem anderen Volume verglichen werden.

Es gibt zwei Arten von Datenträger Kontingent Limits, wie in der folgenden Tabelle dargestellt.



| Begrenzung                        | BESCHREIBUNG                                                                                                                                                                                                                                                                    |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Schwellenwert für Warnung<br/> | Sie können das System so konfigurieren, dass ein System Protokolldatei-Eintrag generiert wird, wenn der Speicherplatz, der dem Benutzer berechnet wird, diesen Wert überschreitet.<br/>                                                                                                                                         |
| Feste Kontingente<br/>        | Sie können das System so konfigurieren, dass ein System Protokolldatei-Eintrag generiert wird, wenn der Speicherplatz, der dem Benutzer berechnet wird, diesen Wert überschreitet. Sie können das System auch so konfigurieren, dass dem Benutzer zusätzlicher Speicherplatz verweigert wird, wenn der Speicherplatz, der dem Benutzer in Rechnung gestellt wird, diesen Wert überschreitet.<br/> |



 

Das NTFS-Dateisystem erstellt automatisch einen Benutzer Kontingent Eintrag, wenn ein Benutzer zum ersten Mal auf das Volume schreibt. Einträge, die automatisch erstellt werden, werden die Standardwerte für Warnungs Schwellenwert und feste Kontingent Grenze für das Volume zugewiesen.

 

 




