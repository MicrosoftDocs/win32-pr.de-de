---
title: D1101 Unbekanntes Handle
ms.assetid: ae40058a-ea17-4262-87dc-0ce852c16c2a
description: Eine Schnittstelle, die nicht von dieser DLL zugeordnet wurde, wurde an sie übergeben.
keywords:
- D1101 Unbekanntes Handle Direct2D
topic_type:
- apiref
api_name:
- D1101 Unknown Handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 37e84b9e5117732784267374ad9e6618e60d3b4020a6d23863b069b3b8233aa1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118161001"
---
# <a name="d1101-unknown-handle"></a>D1101: Unbekanntes Handle

Eine \[ *Schnittstellenschnittstelle,* die \] nicht von dieser DLL zugeordnet wurde, wurde an sie übergeben.

## <a name="placeholders"></a>Platzhalter

<dl> <dt>

<span id="interface"></span><span id="INTERFACE"></span>*Schnittstelle*
</dt> <dd>

Die Adresse der Schnittstelle.

</dd> </dl> 




 

## <a name="possible-causes"></a>Mögliche Ursachen

Ungültige Ressourcenverwendung. Die außerhalb von Direct2D erstellte Ressource wird mit einer Direct2D-Factory verwendet, oder die in einer Factory erstellten Ressourcen wurden mit einer Ressource verwendet, die von einer anderen Factory erstellt wurde.

 

 




