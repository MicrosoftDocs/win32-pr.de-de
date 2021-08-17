---
description: Zertifikatdienste unterstützen die Verwendung von Zertifikaten gemäß der ITU-T-Empfehlung X.509 (auch ISO/IEC 9594-8).
ms.assetid: 59f20de0-de24-43c7-a1a2-bdc91ee28059
title: Zertifikateigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48850b812c8a8227f41229ccbaa88259805d61a199d695f4a90d4652a94b99dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117771565"
---
# <a name="certificate-properties"></a>Zertifikateigenschaften

Zertifikatdienste unterstützen die Verwendung von Zertifikaten gemäß der ITU-T-Empfehlung [*X.509*](../secgloss/x-gly.md) (auch ISO/IEC 9594-8). Im Folgenden finden Sie Eigenschaften, die in einem X.509-Standardzertifikat enthalten sind.



| Feld                                       | Beschreibung                                                                                                                                                                                                     |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version                                     | Versionsnummer des Zertifikatformats.                                                                                                                                                                       |
| Seriennummer                               | Seriennummer des Zertifikats. Diese Nummer wird vom Aussteller zugewiesen und ist in der Liste der ausgestellten Zertifikate des Ausstellers eindeutig.                                                                          |
| Algorithmusbezeichner und Parameter         | Signaturalgorithmus und alle vom Aussteller verwendeten Parameter.                                                                                                                                                      |
| Issuer (Aussteller)                                      | Name der [*Zertifizierungsstelle, die*](../secgloss/c-gly.md) das Zertifikat ausgestellt hat.                                               |
| Not Before (Date)                           | Das Zertifikat ist vor diesem Datum ungültig.                                                                                                                                                                         |
| Nicht nach (Datum)                            | Das Zertifikat ist nach diesem Datum ungültig.                                                                                                                                                                          |
| Antragstellername                                | Name der Person oder Entität, für die bzw. die das Zertifikat ausgestellt wird. Dieses Feld kann auch die Organisation, die Organisationseinheit, den Ort, das Bundesland oder die Provinz sowie das Land/die Region des Zertifikatempfängers enthalten. |
| Algorithmus und Parameter für den öffentlichen Schlüssel des Betreffs | Der Algorithmus und alle Parameter, die für den öffentlichen Schlüssel des [*Subjekts verwendet werden.*](../secgloss/p-gly.md)                                                                       |
| Öffentlicher Schlüssel des Betreffs                          | Der tatsächliche öffentliche Schlüssel (eine Bitzeichenfolge).                                                                                                                                                                           |
| Signatur                                   | Signatur, die vom Aussteller bereitgestellt wird.                                                                                                                                                                            |



 

Ein Zertifikat kann abhängig von der [*X.509-Version*](../secgloss/x-gly.md) des Zertifikats die folgenden Elemente enthalten.



| Optionales Feld    | Beschreibung                                                                                                                                                                                               |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Eindeutige Aussteller-ID  | Wird verwendet, um den Ausstellernamen eindeutig zu machen, wenn er von mehr als einer Entität verwendet wurde. Nur in [*X.509*](../secgloss/x-gly.md) 2.0 oder höher vorhanden.<br/> |
| Eindeutige ID des Betreffs | Wird verwendet, um den Betreffnamen eindeutig zu machen, wenn er von mehr als einer Entität verwendet wurde. Nur in X.509 2.0 oder höher vorhanden.<br/>                                                                     |
| Erweiterungen        | Zum Angeben gewünschter benutzerdefinierter Eigenschaften. Im Zertifikat kann eine beliebige Anzahl von Erweiterungsfeldern enthalten sein. Nur in Version X.509 3.0 vorhanden.<br/>                                            |



 

> [!Note]  
> Microsoft Certificate Services stellt X.509-Zertifikate der Version 3 aus.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Namenseigenschaften](name-properties.md)
</dt> </dl>

 

 
