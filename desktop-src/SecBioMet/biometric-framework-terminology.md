---
title: Terminologie des biometrischen Frameworks
description: Die folgenden Begriffe werden in der dokumentation zur biometrischen Framework-API Windows verwendet.
ms.assetid: D6F2BAF0-8ABB-4810-86B1-A46854FBC328
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cd88fe552d9a53d8bcf214280e5b15a9206532383afa87bfee6fe6dd95c9c8f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127260"
---
# <a name="biometric-framework-terminology"></a>Terminologie des biometrischen Frameworks

Die folgenden Begriffe werden in der dokumentation zur biometrischen Framework-API Windows verwendet.



| Begriff                                                 | Definition                                                                                                                                                                                                                                                        |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Biometrieframework (WBF)<br/>         | Eine Frameworkarchitektur in Windows, die eine konsistente Verwaltungsschnittstelle und Benutzeroberfläche für biometrische Geräte bietet.<br/>                                                                                                                         |
| Windows-Biometriedienst<br/>                 | Ein privilegierter Dienst, der alle biometrischen Geräte mithilfe Windows WBDI-kompatiblen Gerätetreibern verwaltet.<br/>                                                                                                                   |
| Windows Schnittstelle für biometrische Treiber<br/>        | Ein Schnittstellenstandard für Treiber, die Fingerabdrucksensoren verwalten.<br/>                                                                                                                                                                                     |
| Windows Biometrischer Dienstanbieter (WBSP)<br/> | Eine Komponente des Windows Biometrischer Dienst, der eine bestimmte Kategorie biometrischer Technologien verwaltet, z. B. einen Fingerabdruckleser. WBSPs sind in den biometrischen Windows integriert. Sie sind keine Plug-Ins, und BSPs von Drittanbietern werden nicht unterstützt. <br/> |
| Biometrischer Faktor<br/>                          | Ein persönliches Merkmal, das gemessen und zur Identifizierung verwendet werden kann. Beispiele hierfür sind Fingerabdrücke und Handgeometrie.<br/>                                                                                                                           |
| Biometrischer Unterfaktor<br/>                      | Ein qualifizierendes Merkmal, das verwendet werden kann, um einen biometrischen Faktor weiter zu definieren. Um beispielsweise einen Fingerabdruck (biometrischer Faktor) vollständig zu identifizieren, muss angegeben werden, von welchem Finger der Druck stammt (biometrischer Unterfaktor).<br/>             |
| Biometrisches Beispiel<br/>                          | Die Daten, die sich aus der Messung eines einzelnen Merkmals einer einzelnen Person ergeben, z. B. das Bild eines Fingerabdrucks.<br/>                                                                                                              |
| Biometrische Vorlage<br/>                        | Ein statistischer Durchschnitt, der generiert wird, indem mehrere biometrische Stichproben eines einzelnen Merkmals für eine einzelne Person gesammelt werden. Eine Vorlage enthält in der Regel nur die Features, die notwendig sind, um die Übereinstimmung einer neuen Probe zu bestimmen.<br/>             |
| Biometrische Einheit<br/>                            | Ein Softwareobjekt, das ein biometrisches Gerät darstellt und zum Erfassen und Verarbeiten biometrischer Stichproben sowie zum Erstellen, Speichern und Abfangen biometrischer Vorlagen verwendet werden kann.<br/>                                                                                         |
| Sensoradapter<br/>                            | Eine Biometrische Komponenten-Plug-In-Komponente, die eine Standardschnittstelle zum Konfigurieren des Sensors, Erfassen von Stichproben und Steuern des Flusses biometrischer Daten an den Motoradapter bietet.<br/>                                                                 |
| Engine-Adapter<br/>                            | Eine Biometrische Komponenten-Plug-In-Komponente, die eine Stichprobe verarbeitet, indem Daten normalisiert, Features extrahiert und Beispieldaten mit vorhandenen Vorlagen übereinstimmen.<br/>                                                                                                   |
| Speicheradapter<br/>                           | Eine Biometrische Komponenten-Plug-In-Komponente, die Vorlagen speichert, verwaltet und abruft.<br/>                                                                                                                                                                      |
| Biometrischer Informationsdatensatz (BIR)<br/>        | Eine Datenstruktur, die rohe oder verarbeitete biometrische Informationen enthält.<br/>                                                                                                                                                                                 |
| Sensorpool<br/>                               | Eine Sammlung biometrischer Einheiten, die eine gemeinsame Verwaltungsrichtlinie verwenden.<br/>                                                                                                                                                                                 |
| Livetest<br/>                          | Ein Prozess, der überprüft, ob eine biometrische Stichprobe nicht aus einer zuvor erfassten Stichprobe spooft oder wiedergegeben wird.<br/>                                                                                                                          |



 

 

 





