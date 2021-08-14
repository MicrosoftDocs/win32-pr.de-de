---
description: Der &\# 0034; Bitfield&\# 0034; geben Sie ohne Kontextanforderungen ein, dass der Benutzer eine ganze Zahl bereitstellt, deren Wert verwendet wird, um ein oder mehrere Bits in einem Bitfeld festzulegen. Dieser Text kann in einer beliebigen Sprache enthalten sein, die mit der Codepage der Datenbank kompatibel ist.
ms.assetid: 28e1bdb9-a42d-46ce-ad24-71bc22e2d92a
title: Beliebiger Bitfeldtyp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 842c9d1725b2bfe9ef0585cafd085ac1ceba33554899909ae3317af38fd7caac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118381384"
---
# <a name="arbitrary-bitfield-type"></a>Beliebiger Bitfeldtyp

Der Typ "Bitfield" ohne Kontext fordert an, dass der Benutzer eine ganze Zahl bereitstellt, deren Wert verwendet wird, um ein oder mehrere Bits in einem Bitfeld festzulegen. Dieser Text kann in einer beliebigen Sprache enthalten sein, die mit der Codepage der Datenbank kompatibel ist.

Der beliebige Bitfeldtyp des [semantischen Typs](semantic-types.md) ist einer der Bitfield-Typen. Dieser Typ besteht aus einer ganzen Zahl, die vom Benutzer aus einer Reihe von Auswahlmöglichkeiten ausgewählt wird. Das Mergetool ersetzt die ausgewählte ganze Zahl in die Vorlagen, die in der Spalte Wert der [Tabelle ModuleSubsdatenbank](modulesubstitution-table.md)angegeben sind. Um ein konfigurierbares Element dieses Typs anzugeben, sollten Modulautoren den Namen des Elements in die Spalte Name eingeben, "3" in die Spalte Format eingeben, die Spalte Typ leer lassen und die Liste der möglichen ganzen Zahlen in der ContextData-Spalte der [ModuleConfiguration-Tabelle](moduleconfiguration-table.md)eingeben.

Die Spalte Typ ist reserviert und muss NULL sein. Der Eintrag in der ContextData-Spalte für alle Bitfield-Formattypen muss das Format " <mask> aufweisen.<Name>=<value>;<Name>=<value>....", wobei <mask> ein ganzzahliger Wert ist, der die interessanten Bits angibt, <Name> ein lokalisierbarer Anzeigename für die Auswahl ist und <value> ist ein ganzzahliger Dezimalwert. Die Kontextspalte wird im [CMSM-Sonderformat](cmsm-special-format.md) und für alle Bitfeldtypen verwendet. Ein Literalzeichen "=" oder ";" kann in das Feld eingegeben werden, <Name> indem ihm ein umgekehrter Schrägstrich (' ') vorangestellt \\ wird.

 

 



