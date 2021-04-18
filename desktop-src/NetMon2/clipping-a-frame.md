---
description: Sie können angeben, dass der Treiber die Frames Ausschneiden soll.
ms.assetid: a4f53568-684b-48cf-835b-915cefb45a5d
title: Clipping eines Frames
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1507b82ffedeb26939d5d954f116bb009ed0ab41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106351661"
---
# <a name="clipping-a-frame"></a>Clipping eines Frames

Sie können angeben, dass der Treiber die Frames Ausschneiden soll. (Wenn die anderen Erfassungs Filter Abschnitte ausgelassen werden, ist dies möglicherweise die einzige Funktion Ihres Erfassungs Filters). Wenn das Feld **nframebytestocopy** nicht NULL (0) ist, gibt sein Wert an, wie viele Bytes jedes Frame erhalten bleiben. Wenn das Feld 0 (null) ist, wird der gesamte Frame beibehalten.

> [!Note]  
> Sie können einen beliebigen Frame Ausschneiden, der die anderen Teile Ihres Erfassungs Filters durch Festlegen von **nframebytestocopy** übergibt.

 

 

 



