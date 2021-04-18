---
title: Cclsobj. CPP
description: In der Beispiel Anbieter Komponente sind die Funktionen für das Schema Klassenobjekt in cclsobj. cpp enthalten.
ms.assetid: e8cdef8e-c031-49e0-9496-871064aec8bd
ms.tgt_platform: multiple
keywords:
- Csampledsclass
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f23c198413819627ce1fcb5a605bd8e45faae0ce
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340195"
---
# <a name="cclsobjcpp"></a>Cclsobj. CPP

In der Beispiel Anbieter Komponente sind die Funktionen für das Schema Klassenobjekt in cclsobj. cpp enthalten.

Die **csampledsclass** -Klasse ist in dieser Datei definiert. **Csampledsclass** ist mit Methoden und Eigenschaften definiert, die in der folgenden Tabelle aufgeführt sind.



| Methode                      | BESCHREIBUNG                                                                                                                                                                                                |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Csampledsclass**          | Standardkonstruktor.                                                                                                                                                                                      |
| **~ Csampledsclass**         | Standardedekonstruktor.                                                                                                                                                                                       |
| **"Feeclass"**             | Erstellen Sie ein ADS-Schema Klassenobjekt. Such Attribut Definitionen durch Aufrufen von **sampledsgetclassdefinition**.                                                                                                 |
| **"Feeclass"**             | Erstellen Sie ein Schema Klassenobjekt, wenn die Attribut Definitionen vorhanden sind, und legen Sie bekannte Attribute fest, wie z. b. die in [**iadsclass:: mandatoryattribute**](iadsclass-property-methods.md)aufgeführten.                     |
| **"Zugeordnete Zuordnung"**     | Erstellen Sie ein Schema Klassenobjekt, und laden Sie dessen Typdaten.                                                                                                                                                       |
| **QueryInterface**          | Gibt den angeforderten Schnittstellen Zeiger zurück, falls verfügbar.                                                                                                                                                      |
| Standard-IADs-Methoden.      | Standard mäßige [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) -Schnittstellen Methoden, die in dieser Datei enthalten sind.                                                                                                                                     |
| Standard mäßige iadsclass-Methoden. | Standard mäßige [**iadsclass**](/windows/desktop/api/Iads/nn-iads-iadsclass) -Schnittstellen Methoden, die in dieser Datei enthalten sind.                                                                                                                           |
| **"Kreatepropertylist"**      | Erstellen Sie eine Liste von Eigenschaften, die dieser Schema Klasse zugeordnet sind, indem Sie **createpropertyentry** aufrufen.                                                                                                          |
| **"Kreatepropertyentry"**     | Erstellen Sie ein Eigenschafts Objekt in dieser Schema Klasse.                                                                                                                                                           |
| **Freipropertyentry**       | Gibt den in " **kreatepropertyentry**" vorgenommenen Eintrag frei.                                                                                                                                                            |
| **Makevariantfromproplist** | Erstellen Sie ein Array von Varianten aus der von " **kreatepropertylist**" erstellten Eigenschaften Liste. Kann in der Implementierung von [**iadsclass:: mandatoryattributs**](iadsclass-property-methods.md) usw. verwendet werden. |



 

 

 




