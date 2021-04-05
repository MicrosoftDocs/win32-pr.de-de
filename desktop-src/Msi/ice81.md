---
description: ICE81 überprüft die msidigitalcertificate-Tabelle, die msidigitalsignature-Tabelle, die MsiPatchCertificate-Tabelle und die msipackagecertificate-Tabelle.
ms.assetid: 83d8bc62-679e-410f-a95c-ffe13952b710
title: ICE81
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd2fef8da1027fc739ce8e6e979ca998a1cd053a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752792"
---
# <a name="ice81"></a>ICE81

ICE81 überprüft die [msidigitalcertificate](msidigitalcertificate-table.md)-Tabelle, die [msidigitalsignature-Tabelle](msidigitalsignature-table.md), die [MsiPatchCertificate](msipatchcertificate-table.md)-Tabelle und die [msipackagecertificate-Tabelle](msipackagecertificate-table.md). Durch diese benutzerdefinierte Ice-Aktion werden Warnungen für digitale Zertifikate ausgegeben, die nicht verwendet werden oder auf die nicht verwiesen wird. Außerdem wird ein Fehler ausgegeben, wenn das signierte Objekt nicht vorhanden ist oder die CAB-Datei des signierten Objekts nicht auf externe Daten zeigt.

Beachten Sie, dass ICE03 überprüft, ob der Eintrag in der Tabellenspalte in der msidigitalsignature-Tabelle "Media" lautet.

## <a name="result"></a>Ergebnis

ICE81 gibt die folgenden Warnungen für nicht verwendete oder nicht referenzierte digitale Zertifikate aus.



| ICE81-Warnung                                                                                                                                                      | BESCHREIBUNG                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| In den Tabellen msidigitalsignature, msipackagecertificate oder MsiPatchCertificate konnte kein Verweis auf einen der Datensätze in der Tabelle msidigitalcertificate gefunden werden. | Diese Warnung wird zurückgegeben, wenn alle Datensätze nicht verwendet werden.                |
| \[ \] In den Tabellen msidigitalsignature, msipackagecertificate oder MsiPatchCertificate konnte kein Verweis auf das digitale Zertifikat 1 gefunden werden.                         | Diese Warnung wird zurückgegeben, wenn einige Datensätze, aber nicht alle, nicht verwendet werden. |



 

ICE81 gibt die folgenden Fehler aus.



| ICE81-Fehler                                                                                                                                                              | BESCHREIBUNG                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Die Medien Tabelle ist nicht vorhanden. Daher sind alle Einträge in msidigitalsignature falsch.                                                                                   | Das signierte Objekt ist nicht vorhanden. Dieser Fehler wird zurückgegeben, wenn die Medien Tabelle nicht vorhanden ist, aber msidigitalsignature Einträge aufweist.                                |
| Fehlendes signiertes Objekt \[ 2 \] in der Medien Tabelle                                                                                                                               | Das signierte Objekt \[ 2 \] ist nicht vorhanden. Dieser Fehler wird zurückgegeben, wenn die Medien Tabelle vorhanden ist, dieser Eintrag in msidigitalsignature jedoch nicht in der Medien Tabelle vorhanden ist. |
| Der Eintrag in Tabelle \[ 1 \] mit Schlüssel \[ 2 \] wird signiert. Daher sollte die CAB-Seite auf ein Objekt außerhalb des Pakets zeigen (der Wert von CAB sollte nicht mit dem Präfix versehen werden \# ). | Die CAB-Datei des signierten Objekts verweist nicht auf externe Daten. \[1 \] ist der Tabellenname. \[2 \] ist der Schlüssel in der Medien Tabelle.                                             |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ice-Referenz](ice-reference.md)
</dt> </dl>

 

 



