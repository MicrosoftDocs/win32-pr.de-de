---
description: Wird vom Compiler aufgerufen, wenn Ihre Funktion mehrere Seiten lokaler Variablen enthält.
ms.assetid: 154dd992-88b5-44a4-9594-5d13afb71c28
title: _chkstk Routine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b129b73801c6c18b63b10ac61898ee13a9c5d4f1f0422678bbfe5af82d5b44f8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119538834"
---
# <a name="_chkstk-routine"></a>\_chkstk-Routine

Wird vom Compiler aufgerufen, wenn Ihre Funktion mehrere Seiten lokaler Variablen enthält.

## <a name="remarks"></a>Hinweise

\_chkstk Routine ist eine Hilfsroutine für den C-Compiler. Bei x86-Compilern wird chkstk Routine aufgerufen, wenn die lokalen Variablen 4K Bytes überschreiten. Bei x64-Compilern ist \_ dies 8K.

 

 



