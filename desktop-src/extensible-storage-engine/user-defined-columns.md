---
description: 'Weitere Informationen zu: Benutzerdefinierte Spalten'
title: Benutzerdefinierte Spalten
TOCTitle: User Defined Columns
ms:assetid: cccfc97c-acde-4328-a87f-ee7dcc54203c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294091(v=EXCHG.10)
ms:contentKeyID: 32765706
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 57212f49fe97f276677a2ca4396a23d672e175a86eb067f1d276b9c20a46b891
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117890071"
---
# <a name="user-defined-columns"></a>Benutzerdefinierte Spalten


_**Gilt für:** Windows | Windows Server_

## <a name="user-defined-columns"></a>Benutzerdefinierte Spalten

Benutzerdefinierte Spalten sind Spalten, deren Standardwerte von einer Rückruffunktion bereitgestellt werden. Diese Spalten werden immer mit Tags versehen und auf den Wert festgelegt, der von der Rückruffunktion berechnet wird. Dieser Wert muss für jede Zeile in der Tabelle stabil sein. Die Rückruffunktion wird nur verwendet, wenn die Anwendung oder die Datenbank-Engine selbst den Wert der Spalte für eine bestimmte Zeile lesen muss. Die Anwendung hat die Möglichkeit, den Standardwert zu überschreiben und einen bestimmten Wert in der Spalte festzulegen. Wenn der Standardwert in den Spalten überschrieben wird, verwendet er Leerzeichen in der Zeile, andernfalls verwenden benutzerdefinierte Standardspalten keinen Speicherplatz im Datensatz.

Die Option Benutzerdefinierte Standardwerte wird im **grbit-Member** der [JET_COLUMNDEF-Struktur](./jet-columndef-structure.md) im Aufruf von [JetAddColumn](./jetaddcolumn-function.md)festgelegt. Der *pvDefault-Parameter* der [JetAddColumn-Funktion](./jetaddcolumn-function.md) verweist auf eine [JET_USERDEFINEDDEFAULT-Struktur,](./jet-userdefineddefault-structure.md) die den Namen der Rückruffunktion im **szCallback-Member** und die Daten enthält, die an den Rückruf im **pbUserData-Member** übergeben werden.
