---
title: Schleifen Wiedergabe für mciwnd
description: Schleifen Wiedergabe (mciwnd)
ms.assetid: 59e27271-332a-4c62-bfcd-5377cdbf0848
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba2d6a22e917cf764b37444bcaf4afb0393e1c1b
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/02/2021
ms.locfileid: "106370977"
---
# <a name="looping-playback-for-mciwnd"></a>Schleifen Wiedergabe für mciwnd

Mciwnd unterstützt die Wiedergabe als fortlaufende Schleife. Sie können den Inhalt einer Datei oder eines Geräts wiederholt als Schleife wiedergeben, indem Sie das Makro [**mciwndtartrepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetrepeat) in Kombination mit der **Wiedergabe** Schaltfläche auf der Symbolleiste verwenden. Das Videowiedergabe Gerät MCIAVI unterstützt Wiedergabe Schleifen. Verwenden Sie das [**mciwndgetrepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetrepeat) -Makro, um zu bestimmen, ob die fortlaufende Wiedergabe aktiviert wurde.

 

 




