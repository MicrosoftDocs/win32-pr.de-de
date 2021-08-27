---
description: In der folgenden Tabelle sind die Größenbeschränkungen für die verschiedenen Registrierungselemente aufgeführt.
ms.assetid: a6d3a884-f181-46a5-b655-226c68792e08
title: Größenbeschränkungen für Registrierungselemente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c76a11abc80f80a13e0643d7745d211168ecba8bcf06446af9ac842f8351567
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118885233"
---
# <a name="registry-element-size-limits"></a>Größenbeschränkungen für Registrierungselemente

In der folgenden Tabelle sind die Größenbeschränkungen für die verschiedenen Registrierungselemente aufgeführt.



| Registry-Element | Größenlimit                                                                                                                                            |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| Schlüsselname         | 255 Zeichen. Der Schlüsselname enthält den absoluten Pfad des Schlüssels in der Registrierung, der immer bei einem Basisschlüssel beginnt, z.B. HKEY \_ LOCAL \_ MACHINE. |
| Wertname       | 16.383 Zeichen **Windows 2000:** 260 ANSI-Zeichen oder 16.383 Unicode-Zeichen.<br/>                                                       |
| Wert            | Verfügbarer Arbeitsspeicher (aktuelles Format)1 MB (Standardformat)<br/>                                                                                     |
| Struktur             | Eine Registrierungsstruktur kann 512 Ebenen tief sein. Sie können bis zu 32 Ebenen gleichzeitig über einen einzelnen Registrierungs-API-Aufruf erstellen.                                  |



 

Lange Werte (mehr als 2.048 Bytes) sollten in einer Datei gespeichert werden, und der Speicherort der Datei sollte in der Registrierung gespeichert werden. Dies hilft der Registrierung, effizient zu arbeiten.

Der Dateispeicherort kann der Name eines Werts oder die Daten eines Werts sein. Jedem umgekehrten Schrägstrich in der Speicherortzeichenfolge muss ein anderer umgekehrter Schrägstrich als Escapezeichen vorangestellt werden. Geben Sie beispielsweise "C: \\ \\ mydir \\ \\ myfile" an, um die Zeichenfolge "C: \\ mydir \\ myfile" zu speichern. Ein Dateispeicherort kann auch der Name eines Schlüssels sein, wenn er innerhalb des Grenzwerts von 255 Zeichen für Schlüsselnamen liegt und keine umgekehrten Schrägstriche enthält, die in Schlüsselnamen nicht zulässig sind.

 

 




