---
description: Ein X.509-Standardzertifikat enthält Informationen zu Version, Seriennummer, Algorithmusbezeichner, Ausstellername, gültigem Datumsbereich, Antragstellername, Algorithmus und öffentlichem Antragstellerschlüssel sowie optional eindeutige Aussteller-ID, eindeutige Antragsteller-ID und Erweiterungen.
ms.assetid: 91425185-2a06-4040-b83d-c42ee080d55f
title: Zertifikate und CryptoAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8af32073cc3f42bbee07d1702fd1e6044c424ac236cf05ed8374c33757c1408
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117770741"
---
# <a name="certificates-and-cryptoapi"></a>Zertifikate und CryptoAPI

[*CryptoAPI*](../secgloss/c-gly.md) unterstützt die Verwendung von X.509-Zertifikaten gemäß [IETF RFC 3280.](https://www.ietf.org/rfc/rfc3280.txt) In dieser Dokumentation wird davon ausgegangen, dass ein X.509- oder vergleichbares [*digitales Zertifikat*](../secgloss/c-gly.md)verwendet wird.

Ein X.509-Standardzertifikat enthält die folgenden Informationen.



| Feld                | Beschreibung                                                                                                                                                                                                                |
|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version              | Versionsnummer des Zertifikats.                                                                                                                                                                                         |
| Seriennummer        | Seriennummer des Zertifikats.                                                                                                                                                                                          |
| Algorithmusbezeichner | Signaturalgorithmus, der vom Zertifikatsignierer verwendet wird.                                                                                                                                                                        |
| Ausstellername          | Name des Zertifikatausstellers.                                                                                                                                                                                     |
| Nicht vor           | Datum, vor dem das Zertifikat ungültig ist.                                                                                                                                                                            |
| Nicht nach            | Das Datum, nach dem das Zertifikat ungültig ist.                                                                                                                                                                             |
| Antragstellername         | Name der Person oder Entität, für die das Zertifikat ausgestellt wird.                                                                                                                                                      |
| Algorithmus            | Algorithmus, der für den öffentlichen Schlüssel verwendet wird.                                                                                                                                                                                         |
| Öffentlicher Schlüssel des Antragstellers   | Tatsächlicher öffentlicher Schlüssel (eine Bitzeichenfolge).                                                                                                                                                                                          |
| Eindeutige Aussteller-ID     | Optionales Feld. Falls vorhanden, muss version 2 sein.                                                                                                                                                                     |
| Eindeutige Antragsteller-ID    | Optionales Feld. Falls vorhanden, muss version 2 sein.                                                                                                                                                                     |
| Erweiterungen           | Optionales Feld. Stellt zusätzliche Daten dar, die ein Aussteller einem Zertifikat hinzufügen kann, z. B. E-Mail-Adresse oder Autorisierung zum Ausstellen von Zertifikaten. Wenn Erweiterungen vorhanden sind, muss Version 3 vorliegen.<br/> |



 

 

 
