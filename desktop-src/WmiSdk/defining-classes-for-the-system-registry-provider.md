---
description: Eine Verwaltungs Anwendung, die den System Registrierungs Anbieter verwendet, kann Klassen mit Eigenschaften definieren, die Registrierungsdaten für bestimmte Schlüssel darstellen. Anschließend werden die Klassen im WMI-Repository gespeichert.
ms.assetid: e8707a3d-a393-4be0-9e86-297f0af15d99
ms.tgt_platform: multiple
title: Definieren von Klassen für den System Registrierungs Anbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ebce4867559398722182b7b77ae02bc31c070b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960302"
---
# <a name="defining-classes-for-the-system-registry-provider"></a>Definieren von Klassen für den System Registrierungs Anbieter

Eine Verwaltungs Anwendung, die den System Registrierungs Anbieter verwendet, kann Klassen mit Eigenschaften definieren, die Registrierungsdaten für bestimmte Schlüssel darstellen. Anschließend werden die Klassen im WMI-Repository gespeichert. Die meisten Prozesse zum Definieren einer Klasse für die Systemregistrierung sind identisch mit der Definition einer anderen Klasse. Der System Registrierungs Anbieter erfordert jedoch, dass Sie bestimmte Datentypen und Qualifizierer verwenden.

Im folgenden Verfahren wird beschrieben, wie Sie eine Klasse für den System Registrierungs Anbieter definieren.

**So definieren Sie eine Klasse für den System Registrierungs Anbieter**

1.  Erstellen Sie die Klasse wie jede andere Klasse.

    Weitere Informationen finden Sie unter [Creating a Class](creating-a-class.md).

2.  Ordnen Sie die entsprechenden Registrierungs Datentypen den entsprechenden WMI-Typen zu.

    Der System Registrierungs Anbieter ordnet die Registrierungs Datentypen bestimmten WMI-Datentypen zu. Weitere Informationen finden Sie unter [Mapping eines Registrierungs Datentyps zu einem WMI-Datentyp](mapping-a-registry-data-type-to-a-wmi-data-type.md).

3.  Verwenden Sie die erforderlichen Qualifizierer, um den Speicherort des Registrierungs Anbieters und den Speicherort des entsprechenden Registrierungsschlüssels zu definieren.

    Der System Registrierungs Anbieter verwendet drei Qualifizierer, um den Speicherort verschiedener Klassen, Anbieter und Registrierungseinträge zu definieren. Weitere Informationen finden Sie unter [Definieren einer Registrierungs Klasse mit Qualifizierern](defining-a-registry-class-with-qualifiers.md).

 

 



