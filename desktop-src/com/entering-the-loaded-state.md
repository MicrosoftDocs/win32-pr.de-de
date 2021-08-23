---
title: Eingeben des Zustands "Geladen"
description: Eingeben des Zustands "Geladen"
ms.assetid: 841b6f1a-cf9d-4a7e-9732-0701777a9617
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 091d9fe92acbf202c40c1a7ec485f3028bbc22d652ef29db1cb406d961b19e7c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119410250"
---
# <a name="entering-the-loaded-state"></a>Eingeben des Zustands "Geladen"

Wenn ein Objekt in den geladenen Zustand eintritt, werden die In-Memory-Strukturen erstellt, die das Objekt darstellen, damit Vorgänge für das Objekt aufgerufen werden können. Der Handler oder Prozessserver des Objekts wird geladen. Dieser Als Instanziierung bezeichnete Prozess tritt auf, wenn ein Objekt aus dem persistenten Speicher geladen wird (ein Übergang vom passiven zum geladenen Zustand) oder wenn ein Objekt zum ersten Mal erstellt wird. 

Intern handelt es sich bei der Instanziierung um einen zweiphasenbasierten Prozess. Ein Objekt der entsprechenden Klasse wird erstellt, nach dem eine Methode für dieses Objekt aufgerufen wird, um die Initialisierung durchzuführen und Zugriff auf die Daten des Objekts zu geben. Die Initialisierungsmethode wird in einer der unterstützten Schnittstellen des Objekts definiert. Die aufgerufene initialisierungsmethode hängt vom Kontext ab, in dem das Objekt instanziiert wird, und vom Speicherort der Initialisierungsdaten.

 

 




