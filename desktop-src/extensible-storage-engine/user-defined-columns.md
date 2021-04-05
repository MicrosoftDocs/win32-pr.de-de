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
# <a name="user-defined-columns"></a><span data-ttu-id="49b72-103">Benutzerdefinierte Spalten</span><span class="sxs-lookup"><span data-stu-id="49b72-103">User Defined Columns</span></span>


<span data-ttu-id="49b72-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="49b72-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="user-defined-columns"></a><span data-ttu-id="49b72-105">Benutzerdefinierte Spalten</span><span class="sxs-lookup"><span data-stu-id="49b72-105">User Defined Columns</span></span>

<span data-ttu-id="49b72-106">Benutzerdefinierte Spalten sind Spalten, deren Standardwerte von einer Rückruffunktion bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="49b72-106">User defined columns are columns whose default values are provided by a callback function.</span></span> <span data-ttu-id="49b72-107">Diese Spalten werden immer gekennzeichnet und auf den Wert festgelegt, der von der Rückruffunktion berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="49b72-107">These columns are always tagged and set to the value computed by the callback function.</span></span> <span data-ttu-id="49b72-108">Dieser Wert muss für jede Zeile in der Tabelle stabil sein.</span><span class="sxs-lookup"><span data-stu-id="49b72-108">This value must be stable for each row in the table.</span></span> <span data-ttu-id="49b72-109">Die Rückruffunktion wird nur verwendet, wenn die Anwendung oder die Datenbank-Engine selbst den Wert der Spalte für eine bestimmte Zeile lesen muss.</span><span class="sxs-lookup"><span data-stu-id="49b72-109">The callback function is only used when either the application or the database engine itself needs to read the value of the column for a given row.</span></span> <span data-ttu-id="49b72-110">Die Anwendung verfügt über die Möglichkeit, den Standardwert zu überschreiben und einen bestimmten Wert in der Spalte festzulegen.</span><span class="sxs-lookup"><span data-stu-id="49b72-110">The application has the option to override the default value and set a specific value in the column.</span></span> <span data-ttu-id="49b72-111">Wenn der Standardwert in den Spalten überschrieben wird, wird ein Leerzeichen in der Zeile verwendet; andernfalls verwenden benutzerdefinierte Standard Spalten keinen Speicherplatz im Datensatz.</span><span class="sxs-lookup"><span data-stu-id="49b72-111">When the default value is overridden in the columns, it uses space in the row, otherwise user defined default columns do not use space in the record.</span></span>

<span data-ttu-id="49b72-112">Die Option für benutzerdefinierte Standardwerte wird im **grbit** -Member der [JET_COLUMNDEF](./jet-columndef-structure.md) Struktur im Befehl [jetaddcolumn](./jetaddcolumn-function.md)festgelegt.</span><span class="sxs-lookup"><span data-stu-id="49b72-112">User defined defaults option is set in the **grbit** member of the [JET_COLUMNDEF](./jet-columndef-structure.md) structure in the call to [JetAddColumn](./jetaddcolumn-function.md).</span></span> <span data-ttu-id="49b72-113">Der *pvdefault* -Parameter der [jetaddcolumn](./jetaddcolumn-function.md) -Funktion verweist auf eine [JET_USERDEFINEDDEFAULT](./jet-userdefineddefault-structure.md) Struktur, die den Namen der Rückruffunktion im **szcallback** -Member enthält, sowie die Daten, die dem Rückruf im **pbuserdata** -Member übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="49b72-113">The *pvDefault* parameter of the [JetAddColumn](./jetaddcolumn-function.md) function points to a [JET_USERDEFINEDDEFAULT](./jet-userdefineddefault-structure.md) structure, that contains the name of the callback function in the **szCallback** member, and the data that is passed to the callback in the **pbUserData** member.</span></span>
