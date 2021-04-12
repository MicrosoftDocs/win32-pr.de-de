---
description: Sie können keine Instanzen der geänderten Klassen im lokalisierten Namespace erstellen. Geänderte Klassen im lokalisierten Namespace werden so behandelt, als wären Sie abstrakt, obwohl Sie nicht den abstrakten Qualifizierer enthalten.
ms.assetid: a0583153-f5d2-4f4c-ab2e-6ec468e665c7
ms.tgt_platform: multiple
title: Überlegungen zu geänderten Klassen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f77a2caa315ab4878fe619c13c69bd5d2e1a2610
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218816"
---
# <a name="amended-class-considerations"></a>Überlegungen zu geänderten Klassen

Sie können keine Instanzen der geänderten Klassen im lokalisierten Namespace erstellen. Geänderte Klassen im lokalisierten Namespace werden so behandelt, als wären Sie abstrakt, obwohl Sie nicht den [**abstrakten**](standard-qualifiers.md) Qualifizierer enthalten.

Wenn Sie mit dem WBEM-Flag eine geänderte Klasse aus einem lokalisierten Namespace abrufen, indem Sie das \_ \_ Flag "geänderte Qualifizierer" verwenden \_ \_ und eine Instanz daraus erzeugen, enthält die Instanz alle geänderten Qualifizierer der geänderten Klasse. Diese neue Klasse kann nicht im-Namespace gespeichert werden, der die grundlegende Klassendefinition enthält, es sei denn, Sie führen den **Put** -Vorgang mit dem WBEM- \_ Flag \_ Verwenden der \_ geänderten \_ qualifiziererflag Dieses Flag weist WMI an, alle geänderten Qualifizierer zu entfernen, bevor das Objekt gespeichert wird. Wenn Sie das WBEM-Flag nicht für \_ \_ \_ die Verwendung \_ von geänderten Qualifizierern angeben, schlägt der **Put** -Vorgang mit einem WBEM \_ E- \_ \_ Objekt Fehler fehl.

 

 



