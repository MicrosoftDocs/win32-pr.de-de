---
description: 'Weitere Informationen finden Sie hier: benutzerdefinierte Spalten'
title: Benutzerdefinierte Spalten
TOCTitle: User Defined Columns
ms:assetid: cccfc97c-acde-4328-a87f-ee7dcc54203c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294091(v=EXCHG.10)
ms:contentKeyID: 32765706
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 624a916ee2048d9069c7695c79824e3357b511f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041985"
---
# <a name="user-defined-columns"></a>Benutzerdefinierte Spalten


_**Gilt für:** Windows | Windows Server_

## <a name="user-defined-columns"></a>Benutzerdefinierte Spalten

Benutzerdefinierte Spalten sind Spalten, deren Standardwerte von einer Rückruffunktion bereitgestellt werden. Diese Spalten werden immer gekennzeichnet und auf den Wert festgelegt, der von der Rückruffunktion berechnet wird. Dieser Wert muss für jede Zeile in der Tabelle stabil sein. Die Rückruffunktion wird nur verwendet, wenn die Anwendung oder die Datenbank-Engine selbst den Wert der Spalte für eine bestimmte Zeile lesen muss. Die Anwendung verfügt über die Möglichkeit, den Standardwert zu überschreiben und einen bestimmten Wert in der Spalte festzulegen. Wenn der Standardwert in den Spalten überschrieben wird, wird ein Leerzeichen in der Zeile verwendet; andernfalls verwenden benutzerdefinierte Standard Spalten keinen Speicherplatz im Datensatz.

Die Option für benutzerdefinierte Standardwerte wird im **grbit** -Member der [JET_COLUMNDEF](./jet-columndef-structure.md) Struktur im Befehl [jetaddcolumn](./jetaddcolumn-function.md)festgelegt. Der *pvdefault* -Parameter der [jetaddcolumn](./jetaddcolumn-function.md) -Funktion verweist auf eine [JET_USERDEFINEDDEFAULT](./jet-userdefineddefault-structure.md) Struktur, die den Namen der Rückruffunktion im **szcallback** -Member enthält, sowie die Daten, die dem Rückruf im **pbuserdata** -Member übergeben werden.
