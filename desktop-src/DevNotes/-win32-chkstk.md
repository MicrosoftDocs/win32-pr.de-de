---
description: Wird vom Compiler aufgerufen, wenn Sie über mehr als eine Seite lokaler Variablen in der Funktion verfügen.
ms.assetid: 154dd992-88b5-44a4-9594-5d13afb71c28
title: _chkstk-Routine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02a58b31836947dfb1816bea72a54f820354c792
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958127"
---
# <a name="_chkstk-routine"></a>\_chkstk-Routine

Wird vom Compiler aufgerufen, wenn Sie über mehr als eine Seite lokaler Variablen in der Funktion verfügen.

## <a name="remarks"></a>Bemerkungen

\_die chkstk-Routine ist eine Hilfsroutine für den C-Compiler. Bei x86-Compilern \_ wird die chkstk-Routine aufgerufen, wenn die lokalen Variablen 4 KB überschreiten. für x64-Compiler beträgt der Wert 8K.

 

 



