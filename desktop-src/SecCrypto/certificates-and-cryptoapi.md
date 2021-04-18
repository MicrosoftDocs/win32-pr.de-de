---
description: Ein X. 509-Standard Zertifikat, enthält Version, Seriennummer, Algorithmusbezeichner, Aussteller Namen, gültigen Datumsbereich, Antragsteller Namen, Algorithmus und Informationen zum öffentlichen Schlüssel des Antragstellers und optional eine eindeutige Aussteller-ID, eine eindeutige ID des Antragstellers und Erweiterungen.
ms.assetid: 91425185-2a06-4040-b83d-c42ee080d55f
title: Zertifikate und kryptoapi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 325086ab0dd46ace85745ca292bcab9bcd5324e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343802"
---
# <a name="certificates-and-cryptoapi"></a>Zertifikate und kryptoapi

[*CryptoAPI*](../secgloss/c-gly.md) unterstützt die Verwendung von X. 509-Zertifikaten, wie in [IETF RFC 3280](https://www.ietf.org/rfc/rfc3280.txt)definiert. In dieser Dokumentation wird davon ausgegangen, dass ein X. 509-oder ein vergleichbares [*digitales Zertifikat*](../secgloss/c-gly.md)verwendet wird.

Ein X. 509-Standard Zertifikat enthält die folgenden Informationen.



| Feld                | BESCHREIBUNG                                                                                                                                                                                                                |
|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version              | Die Versionsnummer des Zertifikats.                                                                                                                                                                                         |
| Seriennummer        | Seriennummer des Zertifikats.                                                                                                                                                                                          |
| Algorithmusbezeichner | Der Signatur Algorithmus, der vom Zertifikat Bezeichner verwendet wird.                                                                                                                                                                        |
| Ausstellername          | Der Name des Ausstellers des Zertifikats.                                                                                                                                                                                     |
| Nicht vor           | Das Datum, vor dem das Zertifikat ungültig ist.                                                                                                                                                                            |
| Nicht nach            | Das Datum, nach dem das Zertifikat ungültig ist.                                                                                                                                                                             |
| Antragstellername         | Der Name der Person oder Entität, für die das Zertifikat ausgestellt wird.                                                                                                                                                      |
| Algorithmus            | Der Algorithmus, der für den öffentlichen Schlüssel verwendet wird.                                                                                                                                                                                         |
| Öffentlicher Schlüssel des Antragstellers   | Tatsächlicher öffentlicher Schlüssel (Bitzeichenfolge).                                                                                                                                                                                          |
| Eindeutige Aussteller-ID     | Optionales Feld. Falls vorhanden, muss Version 2 lauten.                                                                                                                                                                     |
| Eindeutige Subjekt-ID    | Optionales Feld. Falls vorhanden, muss Version 2 lauten.                                                                                                                                                                     |
| Erweiterungen           | Optionales Feld. Stellt zusätzliche Daten dar, die ein Aussteller einem Zertifikat hinzufügen kann, z. b. eine e-Mail-Adresse oder Autorisierung zum Ausstellen von Zertifikaten. Wenn Erweiterungen vorhanden sind, muss Version 3 sein.<br/> |



 

 

 
