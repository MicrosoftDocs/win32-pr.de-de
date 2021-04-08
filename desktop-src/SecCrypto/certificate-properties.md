---
description: Die Zertifikat Dienste unterstützen die Verwendung von Zertifikaten, wie in der ITU-T-Empfehlung X. 509 (auch ISO/IEC 9594-8) definiert.
ms.assetid: 59f20de0-de24-43c7-a1a2-bdc91ee28059
title: Zertifikateigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbc234f574e0b5bef2d4884706584b5c33ea9c31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864363"
---
# <a name="certificate-properties"></a>Zertifikateigenschaften

Die Zertifikat Dienste unterstützen die Verwendung von Zertifikaten, wie in der ITU-T-Empfehlung [*X. 509*](../secgloss/x-gly.md) (auch ISO/IEC 9594-8) definiert. Die folgenden Eigenschaften sind in einem X. 509-Standard Zertifikat enthalten.



| Feld                                       | BESCHREIBUNG                                                                                                                                                                                                     |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version                                     | Die Versionsnummer des Zertifikats Formats.                                                                                                                                                                       |
| Seriennummer                               | Seriennummer des Zertifikats. Diese Nummer wird vom Aussteller zugewiesen und ist innerhalb der Liste der ausgestellten Zertifikate des Ausstellers eindeutig.                                                                          |
| Algorithmusbezeichner und-Parameter         | Der Signatur Algorithmus und alle Parameter, die vom Aussteller verwendet werden.                                                                                                                                                      |
| Issuer (Aussteller)                                      | Der Name der [*Zertifizierungs*](../secgloss/c-gly.md) Stelle, die das Zertifikat ausgestellt hat.                                               |
| Nicht vor (Datum)                           | Das Zertifikat ist vor diesem Datum ungültig.                                                                                                                                                                         |
| Nicht nach (Datum)                            | Das Zertifikat ist nach diesem Datum ungültig.                                                                                                                                                                          |
| Antragstellername                                | Der Name der Person oder Entität, für die das Zertifikat ausgestellt wird. Dieses Feld kann auch die Organisation, Organisationseinheit, Ort, Bundesstaat, Kanton und Land/Region des Zertifikats Empfängers enthalten. |
| Algorithmus und Parameter für den öffentlichen Schlüssel des Antragstellers | Der Algorithmus und alle Parameter, die für den [*öffentlichen Schlüssel*](../secgloss/p-gly.md)des Antragstellers verwendet werden.                                                                       |
| Öffentlicher Schlüssel des Antragstellers                          | Der tatsächliche öffentliche Schlüssel (eine Bitzeichenfolge).                                                                                                                                                                           |
| Signatur                                   | Die vom Aussteller bereitgestellte Signatur.                                                                                                                                                                            |



 

Abhängig von der [*X. 509*](../secgloss/x-gly.md) -Version des Zertifikats kann ein Zertifikat die folgenden Elemente enthalten.



| Optionales Feld    | BESCHREIBUNG                                                                                                                                                                                               |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Eindeutige Aussteller-ID  | Wird verwendet, um den Aussteller Namen eindeutig zu machen, wenn er von mehr als einer Entität verwendet wurde. Nur in den Versionen [*X. 509*](../secgloss/x-gly.md) 2,0 oder höher vorhanden.<br/> |
| Eindeutige Subjekt-ID | Wird verwendet, um den Antragsteller Namen eindeutig zu machen, wenn er von mehr als einer Entität verwendet wurde. Nur in X. 509 2,0 oder höher vorhanden.<br/>                                                                     |
| Erweiterungen        | Zum angeben gewünschter benutzerdefinierter Eigenschaften. Im Zertifikat können beliebig viele Erweiterungs Felder eingefügt werden. Nur in Version X. 509 3,0 vorhanden.<br/>                                            |



 

> [!Note]  
> Die Microsoft Certificate Services gibt X. 509 Version 3-Zertifikate aus.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Namens Eigenschaften](name-properties.md)
</dt> </dl>

 

 
