---
description: Diese \_ TSPI-Funktion lineSetCurrentLocation ist veraltet. TAPI hat diese Funktion aufgerufen, wenn der Benutzer (mithilfe des Dialogfelds DFÜ-Eigenschaften) oder eine Anwendung (mithilfe der lineSetCurrentLocation-Funktion) den Adressübersetzungsspeicherort geändert hat.
ms.assetid: acd9f05b-88ae-439a-95c0-d1e8779a32fe
title: TSPI_lineSetCurrentLocation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: caa78427bc4892fd0460b60bcb90f5fef43a38f002368c7ca7251cb1ce611c20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012120"
---
# <a name="tspi_linesetcurrentlocation"></a>TSPI \_ lineSetCurrentLocation

Diese \_ TSPI-Funktion lineSetCurrentLocation ist veraltet. TAPI hat diese Funktion aufgerufen,  wenn der Benutzer (mithilfe des Dialogfelds DFÜ-Eigenschaften) oder eine Anwendung (mithilfe der [**lineSetCurrentLocation-Funktion)**](/windows/win32/api/tapi/nf-tapi-linesetcurrentlocation) den Adressübersetzungsspeicherort geändert hat.

Derzeit führt eine Änderung des Übersetzungsorts zu einer LINE DEVSTATE-Nachricht, bei der \_ *dwParam1* auf LINEDEVSTATE \_ TRANSLATECHANGE festgelegt ist.

 

 
