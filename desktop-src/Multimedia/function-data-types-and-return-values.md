---
title: Funktions Datentypen und Rückgabewerte
description: Funktions Datentypen und Rückgabewerte
ms.assetid: a17ec8bb-4369-463f-8c67-11457a18595b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b28bd7484c3d968e92da5fcd19ee738da1ee811a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947636"
---
# <a name="function-data-types-and-return-values"></a>Funktions Datentypen und Rückgabewerte

Die avifile-Funktionen und-Makros verwenden Datei-und Datenstrom Handler, die mit OLE-Technologie implementiert werden. Der Standard Datentyp einer OLE-Funktion ist **STDAPI**, und die Funktion gibt einen **HRESULT** -Wert (0 für Erfolg oder andernfalls einen Fehler) zurück. Wenn eine Funktion einen anderen Wert als ein **HRESULT** zurückgibt, hat der Typ des Prototyps der Funktion eine etwas andere Syntax, die den Rückgabe Werttyp in Klammern nach "STDAPI" einbettet \_ . Beispielsweise wird von einer Funktion, die einen **Long** -Datenwert zurückgibt, **STDAPI \_ (Long)** in der Prototype-Anweisung verwendet.

 

 




