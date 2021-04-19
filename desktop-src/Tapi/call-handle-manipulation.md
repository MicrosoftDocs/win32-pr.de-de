---
description: TAPI bietet eine Reihe von Funktionen zum Bearbeiten von Aufruf Handles und bestimmt die Beziehung zwischen Zeilen, aufrufen und Adressen usw.
ms.assetid: 283fe5e9-689f-4b87-97a6-b345c22ec6a2
title: Bearbeitung von anrufhandles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 248f16088f891b1441626097de5c803a8fe14991
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350571"
---
# <a name="call-handle-manipulation"></a>Bearbeitung von anrufhandles

TAPI bietet eine Reihe von Funktionen zum Bearbeiten von Aufruf Handles und bestimmt die Beziehung zwischen Zeilen, aufrufen und Adressen usw. Die meisten dieser Funktionen werden ausschließlich in TAPI ohne Verweis auf den Dienstanbieter implementiert, mit Ausnahme von [**TSPI \_ linegetcalladressid**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcalladdressid). Diese Funktion Ruft den Adress Bezeichner eines vorhandenen Aufrufes in der Zeile ab. Dienstanbieter, die eine Zeile als Gruppe von Adress bezeichtern modellieren, können eine unvorhersehbare Adresse für einen neuen eingehenden oder ausgehenden Rückruf auswählen. Diese Funktion bietet TAPI ausreichend Informationen, um den [**linegetnewcalls**](/windows/win32/api/tapi/nf-tapi-linegetnewcalls) -Vorgang zu implementieren, wenn er mit der Option "linecallselect Address" aufgerufen wird \_ .

 

 
