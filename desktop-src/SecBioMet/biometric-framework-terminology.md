---
title: Biometrische Framework-Terminologie
description: Die folgenden Begriffe werden in der Windows-Biometrieframework API-Dokumentation verwendet.
ms.assetid: D6F2BAF0-8ABB-4810-86B1-A46854FBC328
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30f150a30915a44dbd59a5a703577e79dc48933f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713446"
---
# <a name="biometric-framework-terminology"></a>Biometrische Framework-Terminologie

Die folgenden Begriffe werden in der Windows-Biometrieframework API-Dokumentation verwendet.



| Begriff                                                 | Definition                                                                                                                                                                                                                                                        |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows-Biometrieframework (WBF)<br/>         | Eine Framework-Architektur in Windows, die eine konsistente Verwaltungsschnittstelle und Benutzeroberfläche für biometrische Geräte bietet.<br/>                                                                                                                         |
| Windows-Biometriedienst<br/>                 | Ein privilegierter Dienst, der alle biometrischen Geräte mithilfe von wbdi-kompatiblen (Windows biometrische Driver Interface) Gerätetreibern verwaltet.<br/>                                                                                                                   |
| Windows-biometrische Treiberschnittstelle<br/>        | Ein Schnittstellenstandard für Treiber, die Fingerabdrucksensoren verwalten.<br/>                                                                                                                                                                                     |
| Windows-Anbieter für biometrische Dienste (wbsp)<br/> | Eine Komponente des Windows-biometrischen Dienstanbieter, die eine bestimmte Kategorie von biometrischen Technologien verwaltet, z. b. ein Fingerabdruckleser Wbsps sind in den Windows-biometrischen Dienst integriert. Sie sind keine Plug-ins, und BSPs von Drittanbietern werden nicht unterstützt. <br/> |
| Biometrischer Faktor<br/>                          | Ein persönliches Merkmal, das gemessen und zur Identifizierung verwendet werden kann. Beispiele hierfür sind Fingerabdrücke und Handgeometrie.<br/>                                                                                                                           |
| Biometrischer unter Faktor<br/>                      | Ein qualifizierendes Merkmal, das zum weiteren Definieren eines biometrischen Faktors verwendet werden kann. Um z. b. einen Fingerabdruck (biometrischer Faktor) vollständig zu identifizieren, ist es erforderlich, den Finger anzugeben, von dem der Druck stammt (biometrischer unter Faktor).<br/>             |
| Biometrisches Beispiel<br/>                          | Die Daten, die sich aus der Messung eines einzelnen Merkmals aus einer einzelnen Person ergeben, z. b. die Abbildung eines Fingerabdrucks.<br/>                                                                                                              |
| Biometrische Vorlage<br/>                        | Ein statistischer Durchschnitt, der durch das Erfassen mehrerer biometrischer Stichproben eines einzelnen Merkmals für eine einzelne Person generiert wird. Eine Vorlage enthält in der Regel nur die Features, die notwendig sind, um die Übereinstimmung einer neuen Probe zu bestimmen.<br/>             |
| Biometrische Einheit<br/>                            | Ein Software Objekt, das ein biometrisches Gerät darstellt und zum Erfassen und Verarbeiten von biometrischen Beispielen und zum Erstellen, speichern und abgleichen biometrischer Vorlagen verwendet werden kann.<br/>                                                                                         |
| Sensor Adapter<br/>                            | Eine Komponente des biometrischen Einheiten-Plug-ins, die eine Standardschnittstelle zum Konfigurieren des Sensors, zum Erfassen von Beispielen und zum Steuern des Ablaufs der biometrischen Daten an den Engine-Adapter bereitstellt.<br/>                                                                 |
| Engine-Adapter<br/>                            | Eine Komponente für biometrische Einheiten-Plug-ins, die ein Beispiel verarbeitet, indem Daten normalisiert, Features extrahiert und Beispiel Daten mit vorhandenen Vorlagen abgeglichen werden.<br/>                                                                                                   |
| Speicheradapter<br/>                           | Eine Komponente des biometrischen Einheiten-Plug-ins, die Vorlagen speichert, verwaltet und abruft.<br/>                                                                                                                                                                      |
| Biometrischer Informationsdaten Satz (BIR)<br/>        | Eine Datenstruktur, die Rohdaten oder verarbeitete biometrische Informationen enthält.<br/>                                                                                                                                                                                 |
| Sensor Pool<br/>                               | Eine Sammlung biometrischer Einheiten, die über eine gemeinsame Verwaltungs Richtlinie verfügen.<br/>                                                                                                                                                                                 |
| Lichtungs Tests<br/>                          | Ein Prozess, mit dem überprüft wird, ob ein biometrisches Beispiel nicht aus einem zuvor gesammelten Beispiel manipuliert oder wiedergegeben wird.<br/>                                                                                                                          |



 

 

 





