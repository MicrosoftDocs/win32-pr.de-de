---
title: Verwenden des/robust-Flags
description: Kompilieren Sie IDL-Dateien immer mithilfe des/robust-Schalters.
ms.assetid: bb2fd026-3ad8-4bb5-b05e-4835b874882f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db395841842331d9297a782fdcd8ea7573139f9e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948880"
---
# <a name="use-the-robust-flag"></a>Verwenden des/robust-Flags

Kompilieren Sie IDL-Dateien immer mithilfe des [**/robust**](/windows/desktop/Midl/-robust) -Schalters. Durch die Verwendung des **/robust** -Schalters werden zusätzliche Informationen generiert, mit denen die Engine für die Netzwerkdaten Darstellung die Lauf Zeit Fehlerüberprüfung für korrelierte Argumente in dynamischen Arrays, Unions und in out-Schnittstellen Zeigern in com-und RPC-Anwendungen ausführen kann. Wenn die Kompilierung von Software mit diesem Flag nicht möglich ist, ist die Software so verfügbar, dass Sie nicht durch Aktivitäten in einem anderen Bereich geschützt werden kann.

 

 