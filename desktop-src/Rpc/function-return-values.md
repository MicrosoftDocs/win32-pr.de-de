---
title: Funktions-Rückgabewerte
description: Funktions-Rückgabewerte ähneln \out\-only-Parametern, da ihre Daten nicht von der Clientanwendung bereitgestellt werden.
ms.assetid: 98d8d228-7222-49bf-9f29-7749a7a76d5a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 525c63422b058da5267003711efa612814907eb91ced353bd78ee78a820a7377
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021000"
---
# <a name="function-return-values"></a>Funktions-Rückgabewerte

Funktions-Rückgabewerte ähneln **\[ \] out-only-Parametern,** da ihre Daten nicht von der Clientanwendung bereitgestellt werden. Sie werden jedoch unterschiedlich verwaltet. Im **\[ Gegensatz zu \]** out-only-Parametern müssen sie keine Zeiger sein. Die Remoteprozedur kann einen beliebigen gültigen Datentyp mit Ausnahme von Verweiszeige und nicht kapselten Unions zurückgeben.

Es wird jedoch empfohlen, **\[ einen \] out-Parameter** anstelle eines Rückgabewerts für komplexe Datentypen zu verwenden. Beim Zurückgeben komplexer Datentypen generiert der MIDL-Compiler einen Stub im /Os-Modus. Daher gehen alle kürzlich von /robust bereitgestellten Informationen zur Fehlerüberprüfung verloren.

Funktions-Rückgabewerte, die Zeigertypen sind, werden vom Clientstub mit einem Aufruf von [midl \_ user allocate \_ zugeordnet.](/windows/desktop/Midl/midl-user-allocate-1) Entsprechend kann nur das eindeutige oder vollständige Zeigerattribut auf einen Zeigerfunktions-Rückgabetyp angewendet werden.

 

 