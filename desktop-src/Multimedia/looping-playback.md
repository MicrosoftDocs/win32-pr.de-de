---
title: Schleifenwiedergabe für MCIWnd
description: Schleifenwiedergabe (MCIWnd)
ms.assetid: 59e27271-332a-4c62-bfcd-5377cdbf0848
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef9144cd17886ff9d6f59bc38311481335a9ae581e5464d7feda0e7fd1a4ec2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118139291"
---
# <a name="looping-playback-for-mciwnd"></a>Schleifenwiedergabe für MCIWnd

MCIWnd unterstützt die Wiedergabe als fortlaufende Schleife. Sie können den Inhalt einer Datei oder eines Geräts wiederholt als Schleife wiedergeben, indem Sie das [**MCIWndSetRepeat-Makro**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetrepeat) in Kombination mit **der** Wiedergabeschaltfläche auf der Symbolleiste verwenden. Das Videowiedergabegerät MCIAVI unterstützt Wiedergabeschleifen. Verwenden Sie das [**MCIWndGetRepeat-Makro,**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetrepeat) um zu ermitteln, ob die fortlaufende Wiedergabe aktiviert wurde.

 

 




