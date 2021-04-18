---
title: D1101 unbekanntes handle
ms.assetid: ae40058a-ea17-4262-87dc-0ce852c16c2a
description: Eine Schnittstelle, die nicht von dieser DLL zugewiesen wurde, wurde an Sie übermittelt.
keywords:
- D1101 unbekanntes handle Direct2D
topic_type:
- apiref
api_name:
- D1101 Unknown Handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 2a87491a02d3dea992f8dd767ad34cf83b2cbf40
ms.sourcegitcommit: 80ee822f6ebcbcc8f60042e0d14a39ef6989c731
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/27/2021
ms.locfileid: "106368703"
---
# <a name="d1101-unknown-handle"></a>D1101: Unbekanntes handle

Eine Schnitt \[ *Stelle* \] , die von dieser DLL nicht zugeordnet wurde, wurde an Sie übermittelt.

## <a name="placeholders"></a>Platzhalter

<dl> <dt>

<span id="interface"></span><span id="INTERFACE"></span>*berfläche*
</dt> <dd>

Die Adresse der-Schnittstelle.

</dd> </dl> 




 

## <a name="possible-causes"></a>Mögliche Ursachen

Ungültige Ressourcenverwendung. Die Ressource, die außerhalb von Direct2D erstellt wurde, wird mit einer Direct2D-Factory verwendet, oder die auf einer Factory erstellten Ressourcen wurden mit einer Ressource verwendet, die von einer anderen Factory erstellt wurde.

 

 




