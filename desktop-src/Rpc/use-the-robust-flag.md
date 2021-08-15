---
title: Verwenden des Flags /robust
description: Kompilieren Sie IDL-Dateien immer mit dem Schalter /robust.
ms.assetid: bb2fd026-3ad8-4bb5-b05e-4835b874882f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab3d6a7c93cbd97e2c65cc83e6933b3204dddbcf2c0e088dfbc0d98bbdb6628d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010888"
---
# <a name="use-the-robust-flag"></a>Verwenden des Flags /robust

Kompilieren Sie IDL-Dateien immer mit dem [**Schalter /robust.**](/windows/desktop/Midl/-robust) Die Verwendung des Schalters **/robust** generiert zusätzliche Informationen, die es der NDR-Engine (Network Data Representation) ermöglichen, Laufzeitfehlerüberprüfungen für korrelierte Argumente in dynamischen Arrays, Unions und out-Schnittstellenzeige in COM- und RPC-Anwendungen durchzuführen. Wenn software nicht mit diesem Flag kompiliert werden kann, ist die Software so angriffs ausgesetzt, dass sie von keinem anderen Bereich geschützt werden kann.

 

 