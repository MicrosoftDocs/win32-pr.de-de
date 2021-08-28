---
description: Sie können keine Instanzen der geänderten Klassen im lokalisierten Namespace erstellen. Geänderte Klassen im lokalisierten Namespace werden so behandelt, als ob sie abstrakt sind, obwohl sie nicht den Abstract-Qualifizierer enthalten.
ms.assetid: a0583153-f5d2-4f4c-ab2e-6ec468e665c7
ms.tgt_platform: multiple
title: Überlegungen zu geänderten Klassen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30cd38bc6134c4fd3596cc36e8a7638eaa1fd6ed264c90302d921a391982e5d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118320240"
---
# <a name="amended-class-considerations"></a>Überlegungen zu geänderten Klassen

Sie können keine Instanzen der geänderten Klassen im lokalisierten Namespace erstellen. Geänderte Klassen im lokalisierten Namespace werden so behandelt, als [](standard-qualifiers.md) ob sie abstrakt sind, obwohl sie nicht den Abstract-Qualifizierer enthalten.

Wenn Sie eine geänderte Klasse aus einem lokalisierten Namespace abrufen, indem Sie das Flag WBEM-FLAG USE AMENDED QUALIFIERS verwenden und eine -Instanz daraus erstellen, enthält die Instanz alle geänderten Qualifizierer der geänderten \_ \_ \_ \_ Klasse. Sie können diese neue Klasse nicht in dem Namespace speichern, der die grundlegende Klassendefinition enthält, es sei denn, Sie führen den **Put-Vorgang** mit dem WBEM-FLAG \_ \_ \_ USE-QUALIFIERS-Flag \_ AUS. Dieses Flag weist WMI an, alle geänderten Qualifizierer vor dem Speichern des Objekts zu verwerfen. Wenn Sie kein WBEM-FLAG \_ \_ \_ USE-ÄNDERBAR QUALIFIERS angeben, schlägt der Put-Vorgang mit einem \_ WBEM  \_ \_ E-ÄNDEROBJEKT-Fehler \_ fehl.

 

 



