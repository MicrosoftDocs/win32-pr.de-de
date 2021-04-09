---
description: Der &\# 0034; Bitfield&\# 0034; geben Sie ohne Kontext Anforderungen ein, dass der Benutzer eine ganze Zahl bereitstellt, deren Wert verwendet wird, um ein oder mehrere Bits in einem Bitfeld festzulegen. Dieser Text kann in jeder Sprache vorliegen, die mit der Codepage der Datenbank kompatibel ist.
ms.assetid: 28e1bdb9-a42d-46ce-ad24-71bc22e2d92a
title: Beliebiger Bitfeldtyp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6571b8585c94577927df8cfedaded802a67d125
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131496"
---
# <a name="arbitrary-bitfield-type"></a>Beliebiger Bitfeldtyp

Der Bitfield-Typ ohne Kontext Anforderungen, dass der Benutzer eine ganze Zahl bereitstellt, mit deren Wert ein oder mehrere Bits in einem Bitfeld festgelegt werden. Dieser Text kann in jeder Sprache vorliegen, die mit der Codepage der Datenbank kompatibel ist.

Der beliebige Bitfeldtyp des [semantischen Typs](semantic-types.md) ist einer der Bitfield-Typen. Dieser Typ besteht aus einer vom Benutzer ausgewählten Ganzzahl aus einem Satz von Optionen. Das Merge-Tool ersetzt die ausgewählte Ganzzahl in den Vorlagen, die in der Spalte Wert der [Tabelle ModuleSubstitution](modulesubstitution-table.md)angegeben sind. Wenn Sie ein konfigurierbares Element dieses Typs angeben möchten, geben Modul Autoren den Namen des Elements in die Spalte Name ein, geben Sie "3" in die Spalte Format ein, lassen Sie die Spalte Typ leer, und geben Sie die Liste möglicher ganzer Zahlen in der Spalte "ContextData" der [Tabelle "ModuleConfiguration](moduleconfiguration-table.md)" ein.

Die Typspalte ist reserviert und muss NULL sein. Der Eintrag in der ContextData-Spalte für alle Bitfield-Format Typen muss das Format aufweisen <mask> .<Name>=<value>;<Name>=<value>.... ", wobei <mask> ein ganzzahliger Wert ist, der die Bits von Interesse angibt, <Name> ist ein Lokalisier barer Anzeige Name für die Auswahl, und <value> ist ein ganzzahliger ganzzahliger Wert. Die Kontext Spalte verwendet das [spezielle cmsm-Format](cmsm-special-format.md) und für alle Bitfeld-Typen. Ein literales Zeichen "=" oder ";" kann im Feld eingegeben werden, <Name> indem es einem umgekehrten Schrägstrich ("") vorangestellt wird \\ .

 

 



