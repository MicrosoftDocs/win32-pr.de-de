---
description: Es gibt eine weitere Klasse von asynchronen Ereignissen neben den oben beschriebenen.
ms.assetid: eaf4b014-1cab-4707-b750-9088e745083e
title: Asynchrone, spontane Ereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd923ba7759ca88994fbf541c9f912ec660a7552
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356276"
---
# <a name="asynchronous-spontaneous-events"></a>Asynchrone, spontane Ereignisse

Es gibt eine weitere Klasse von asynchronen Ereignissen neben den oben beschriebenen. Diese Ereignisse sind "spontan" in dem Sinne, dass Sie keine direkten Ergebnisse der entsprechenden Anforderungen sind. Diese Ereignisse werden in solchen Fällen erkannt, wenn ein eingehender Anruf eingeht oder wenn ein ausgehender Anruf von einem "Klingeln" in den Status "antwortet" wechselt. Wenn TAPI zuerst Interaktionen mit dem TSPI für ein bestimmtes Gerät initialisiert, übergibt es einen Zeiger auf eine Rückruf Prozedur, die aufgerufen wird, um solche spontanen Ereignisse zu melden. Zusammen mit diesem Prozedur Zeiger ist ein Geräte handle, das der Dienstanbieter als einen der tatsächlichen Parameter des Rückrufs enthält.

 

 



