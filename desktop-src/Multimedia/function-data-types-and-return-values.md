---
title: Funktionsdatentypen und Rückgabewerte
description: Funktionsdatentypen und Rückgabewerte
ms.assetid: a17ec8bb-4369-463f-8c67-11457a18595b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74d85ed42a0751147a1a6a61a078ac0899ce0b5756467005fd02ec72d6190096
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117988315"
---
# <a name="function-data-types-and-return-values"></a>Funktionsdatentypen und Rückgabewerte

Die AVIFile-Funktionen und -Makros verwenden Datei- und Streamhandler, die mit OLE-Technologie implementiert werden. Der Standarddatentyp einer OLE-Funktion ist **STDAPI,** und die Funktion gibt einen **HRESULT-Wert** zurück (null für Erfolg oder andernfalls ein Fehler). Wenn eine Funktion einen anderen Wert als **HRESULT** zurückgibt, weist der Typ des Funktionsprototyps eine etwas andere Syntax auf, die den Rückgabewerttyp nach "STDAPI" in Klammern einbettet. \_ Beispielsweise verwendet eine Funktion, die einen **LONG-Datenwert** zurückgibt, **STDAPI \_ (LONG)** in der prototype-Anweisung.

 

 




