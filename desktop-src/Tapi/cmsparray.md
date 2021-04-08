---
description: Die cmsparray-Vorlage implementiert ein intelligentes Array, das Bedarfs gesteuert vergrößert wird.
ms.assetid: 9b30885c-01a4-4aea-a1c3-5d7966e4697f
title: Cmsparray
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a6c14d4bdc0b57a295efa5bcc2adfd79d23d31d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103959849"
---
# <a name="cmsparray"></a>Cmsparray

Die cmsparray-Vorlage implementiert ein intelligentes Array, das Bedarfs gesteuert vergrößert wird. Es ist so konzipiert, dass kleine Arrays mit einfachen Datentypen enthalten sind. Es weist keinen kritischen Abschnitt auf. Die einzigen Abhängigkeiten sind **rezuzuweisungen** und **memmove**. Sie wird intern verwendet, um Listen von Objekt Zeigern beizubehalten. Sie ähnelt der **CSimpleArray** -Implementierung von ATL, ist aber für anfängliche Zuordnungen effizienter.

Diese Vorlage ist in "msputils. h" definiert.

 

 



