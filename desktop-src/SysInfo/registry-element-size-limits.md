---
description: In der folgenden Tabelle sind die Größenbeschränkungen für die verschiedenen Registrierungs Elemente aufgeführt.
ms.assetid: a6d3a884-f181-46a5-b655-226c68792e08
title: Größenbeschränkungen für das Registrierungs Element
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 262609a64e60536dcfc41f29e5d94ea499158861
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358520"
---
# <a name="registry-element-size-limits"></a>Größenbeschränkungen für das Registrierungs Element

In der folgenden Tabelle sind die Größenbeschränkungen für die verschiedenen Registrierungs Elemente aufgeführt.



| Registry-Element | Größenlimit                                                                                                                                            |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| Schlüsselname         | 255 Zeichen. Der Schlüssel Name enthält den absoluten Pfad des Schlüssels in der Registrierung, der immer mit einem Basis Schlüssel beginnt, z. b. HKEY \_ local \_ Machine. |
| Wertname       | 16.383 Zeichen **Windows 2000:** 260 ANSI-Zeichen oder 16.383 Unicode-Zeichen.<br/>                                                       |
| Wert            | Verfügbarer Arbeitsspeicher (Aktuelles Format) 1 MB (Standardformat)<br/>                                                                                     |
| Struktur             | Eine Registrierungs Struktur kann 512 Ebenen tief sein. Sie können bis zu 32 Ebenen gleichzeitig über einen einzigen Registrierungs-API-Aufruf erstellen.                                  |



 

Lange Werte (mehr als 2.048 bytes) sollten in einer Datei gespeichert werden, und der Speicherort der Datei sollte in der Registrierung gespeichert werden. Dadurch kann die Registrierung effizient durchgeführt werden.

Der Speicherort der Datei kann der Name eines Werts oder die Daten eines Werts sein. Jedem umgekehrten Schrägstrich in der Zeichenfolge muss ein anderer umgekehrter Schrägstrich als Escapezeichen vorangestellt werden. Geben Sie z. b. "c: \\ \\ " MyDir " \\ \\ MyFile" an, um die Zeichenfolge "c: \\ " MyDir " \\ MyFile" zu speichern. Bei einem Datei Speicherort kann es sich auch um den Namen eines Schlüssels handeln, wenn er sich innerhalb der 255-Zeichen Beschränkung für Schlüsselnamen befindet und keine umgekehrten Schrägstriche enthält, die in Schlüsselnamen nicht zulässig sind.

 

 




