---
description: Um die Elemente eines Pfads abzurufen, rufen Sie die pdhparser-counterpath-Funktion auf. Die-Funktion analysiert die Elemente eines Counter-Pfads und gibt Sie in einer PDH- \_ counter- \_ Pfad \_ Elementstruktur zurück.
ms.assetid: 65c722f9-6f9d-4e3d-abf3-867cf260ef9f
title: Abrufen von Counter-Pfad Elementen aus einem Counter-Pfad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08b8579033ddf7a97aec36b88bd067f9a240506d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106362470"
---
# <a name="obtaining-counter-path-elements-from-a-counter-path"></a>Abrufen von Counter-Pfad Elementen aus einem Counter-Pfad

Um die Elemente eines Pfads abzurufen, rufen Sie die [**pdhparser-counterpath**](/windows/desktop/api/Pdh/nf-pdh-pdhparsecounterpatha) -Funktion auf. Die-Funktion analysiert die Elemente eines Counter-Pfads und gibt Sie in einer [**PDH- \_ counter- \_ Pfad \_ Element**](/windows/desktop/api/Pdh/ns-pdh-pdh_counter_path_elements_a) Struktur zurück.

Wenn Sie über einen komplexen Instanznamen verfügen (einen, der eine übergeordnete Instanz und einen Instanzindex enthält), können Sie die [**pdhparser seinstancename**](/windows/desktop/api/Pdh/nf-pdh-pdhparseinstancenamea) -Funktion aufrufen, um den Instanznamen, den Instanzindex und den übergeordneten Namen zu extrahieren.

 

 



