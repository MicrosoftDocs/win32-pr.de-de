---
description: ICE81 überprüft die Tabelle MsiDigitalCertificate, die MsiDigitalSignature-Tabelle, die MsiPatchCertificate-Tabelle und die MsiPackageCertificate-Tabelle.
ms.assetid: 83d8bc62-679e-410f-a95c-ffe13952b710
title: ICE81
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97bcf3228282339acd76ae4f20638cc24aeddf5279212b91aca0ece2b21867d8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119580810"
---
# <a name="ice81"></a>ICE81

ICE81 überprüft die [Tabelle MsiDigitalCertificate,](msidigitalcertificate-table.md)die [MsiDigitalSignature-Tabelle,](msidigitalsignature-table.md) [die MsiPatchCertificate-Tabelle](msipatchcertificate-table.md)und die [MsiPackageCertificate-Tabelle.](msipackagecertificate-table.md) Diese benutzerdefinierte ICE-Aktion sendet Warnungen für nicht verwendete oder nicht referenzierte digitale Zertifikate und gibt einen Fehler aus, wenn das signierte Objekt nicht vorhanden ist oder wenn das Cab des signierten Objekts nicht auf externe Daten verweist.

Beachten Sie, dass ICE03 überprüft, ob der Eintrag in der Spalte Table in der MsiDigitalSignature-Tabelle "Media" ist.

## <a name="result"></a>Ergebnis

ICE81 gibt die folgenden Warnungen für nicht verwendete oder nicht referenzierte digitale Zertifikate aus.



| ICE81-Warnung                                                                                                                                                      | Beschreibung                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| In den Tabellen MsiDigitalSignature, MsiPackageCertificate oder MsiPatchCertificate konnte kein Verweis auf datensätze in der MsiDigitalCertificate-Tabelle gefunden werden. | Diese Warnung wird zurückgegeben, wenn alle Datensätze nicht verwendet werden.                |
| In den Tabellen \[ \] MsiDigitalSignature, MsiPackageCertificate oder MsiPatchCertificate konnte kein Verweis auf das digitale Zertifikat 1 gefunden werden.                         | Diese Warnung wird zurückgegeben, wenn einige Datensätze, aber nicht alle, nicht verwendet werden. |



 

ICE81 gibt die folgenden Fehler aus.



| ICE81-Fehler                                                                                                                                                              | Beschreibung                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Die Medientabelle ist nicht vorhanden. Daher sind alle Einträge in MsiDigitalSignature falsch.                                                                                   | Das signierte Objekt ist nicht vorhanden. Dieser Fehler wird zurückgegeben, wenn die Tabelle Media nicht vorhanden ist, MsiDigitalSignature jedoch Einträge aufweist.                                |
| Fehlendes signiertes Objekt \[ 2 \] in der Medientabelle                                                                                                                               | Das signierte Objekt \[ 2 \] ist nicht vorhanden. Dieser Fehler wird zurückgegeben, wenn die Media-Tabelle vorhanden ist, aber dieser Eintrag in MsiDigitalSignature in der Media-Tabelle nicht vorhanden ist. |
| Der Eintrag in Tabelle \[ 1 \] mit Schlüssel \[ 2 ist \] signiert. Daher sollte das Gehäuse auf ein Objekt außerhalb des Pakets zeigen (dem Wert von Cabinet sollte NICHT das Präfix vorangestellt \# werden). | Das Cab des signierten Objekts verweist nicht auf externe Daten. \[1 \] ist der Tabellenname. \[2 \] ist der Schlüssel in der Tabelle Media.                                             |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ICE-Referenz](ice-reference.md)
</dt> </dl>

 

 



