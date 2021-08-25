---
description: Sie können angeben, dass der Treiber die Frames ausschneiden soll.
ms.assetid: a4f53568-684b-48cf-835b-915cefb45a5d
title: Clipping a Frame
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9251fc6f8a1c9612a9fa7301ea8948956291ad0d074f90ff2ccbbf3f799bd2b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911260"
---
# <a name="clipping-a-frame"></a>Clipping a Frame

Sie können angeben, dass der Treiber die Frames ausschneiden soll. (Wenn die anderen Erfassungsfilterabschnitte weggelassen werden, ist dies möglicherweise die einzige Funktion Ihres Erfassungsfilters.) Wenn das **nFrameBytesToCopy-Feld** nicht 0 (null) ist, gibt der Wert an, wie viele Bytes jedes empfangenen Frames beibehalten werden. Wenn das Feld 0 (null) ist, wird der gesamte Frame beibehalten.

> [!Note]  
> Sie können jeden Frame beschneiden, der die anderen Teile des Erfassungsfilters übergibt, indem Sie **nFrameBytesToCopy festlegen.**

 

 

 



