---
description: Rufen Sie die PdhParseCounterPath-Funktion auf, um die Elemente eines Pfads abzurufen. Die Funktion analysiert die Elemente eines Indikatorpfads und gibt sie in einer PDH \_ COUNTER \_ PATH \_ ELEMENTS-Struktur zurück.
ms.assetid: 65c722f9-6f9d-4e3d-abf3-867cf260ef9f
title: Abrufen von Indikatorpfadelementen aus einem Indikatorpfad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 479c8df5c7176684fc439f632a22f829afe5afae202f7595579350450ee30c8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143973"
---
# <a name="obtaining-counter-path-elements-from-a-counter-path"></a>Abrufen von Indikatorpfadelementen aus einem Indikatorpfad

Rufen Sie die [**PdhParseCounterPath-Funktion auf,**](/windows/desktop/api/Pdh/nf-pdh-pdhparsecounterpatha) um die Elemente eines Pfads abzurufen. Die Funktion analysiert die Elemente eines Indikatorpfads und gibt sie in einer [**PDH \_ COUNTER PATH \_ \_ ELEMENTS-Struktur**](/windows/desktop/api/Pdh/ns-pdh-pdh_counter_path_elements_a) zurück.

Wenn Sie über einen komplexen Instanznamen verfügen (einen, der eine übergeordnete Instanz und einen Instanzindex enthält), können Sie die [**PdhParseInstanceName-Funktion**](/windows/desktop/api/Pdh/nf-pdh-pdhparseinstancenamea) aufrufen, um den Instanznamen, den Instanzindex und den übergeordneten Namen zu extrahieren.

 

 



