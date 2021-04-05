---
description: Diese TSPI \_ linesetcurrentlocation-Funktion ist veraltet. TAPI hat diese Funktion aufgerufen, wenn der Benutzer (im Dialogfeld Wähl Eigenschaften) oder eine Anwendung (mithilfe der linesetcurrentlocation-Funktion) den Speicherort der Adressübersetzung geändert hat.
ms.assetid: acd9f05b-88ae-439a-95c0-d1e8779a32fe
title: TSPI_lineSetCurrentLocation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a2361135770ac2d3900a902e0b7fa4fecad511f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757003"
---
# <a name="tspi_linesetcurrentlocation"></a>TSPI \_ linesetcurrentlocation

Diese TSPI \_ linesetcurrentlocation-Funktion ist veraltet. TAPI hat diese Funktion aufgerufen, wenn der Benutzer (im Dialogfeld **Wähl Eigenschaften** ) oder eine Anwendung (mithilfe der [**linesetcurrentlocation**](/windows/win32/api/tapi/nf-tapi-linesetcurrentlocation) -Funktion) den Speicherort der Adressübersetzung geändert hat.

Aktuell führt eine Änderung des Übersetzungsspeicher Orts zu einer Zeile \_ DevState-Nachricht, bei der *dwParam1* auf linedevstate \_ translatechange festgelegt ist.

 

 
