---
title: Eingabe des geladenen Zustands
description: Eingabe des geladenen Zustands
ms.assetid: 841b6f1a-cf9d-4a7e-9732-0701777a9617
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: add74927d107d7f6b9fe2d76856adec6697a00c3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709443"
---
# <a name="entering-the-loaded-state"></a>Eingabe des geladenen Zustands

Wenn ein Objekt in den geladenen Zustand wechselt, werden die in-Memory-Strukturen erstellt, die das Objekt darstellen, sodass Vorgänge für das Objekt aufgerufen werden können. Der Handler des-Objekts oder der in-Process-Server wird geladen. Dieser Prozess, der als *Instanziierung* bezeichnet wird, tritt auf, wenn ein Objekt aus dem permanenten Speicher geladen wird (ein Übergang von dem passiven in den geladenen Zustand) oder wenn ein Objekt zum ersten Mal erstellt wird.

Intern handelt es sich bei der Instanziierung um einen zweistufigen Prozess. Ein Objekt der entsprechenden Klasse wird erstellt, nach dem eine Methode für dieses Objekt aufgerufen wird, um die Initialisierung auszuführen und Zugriff auf die Daten des Objekts zu erhalten. Die Initialisierungs Methode wird in einer der unterstützten Schnittstellen des Objekts definiert. Die jeweilige Initialisierungs Methode, die aufgerufen wird, hängt vom Kontext ab, in dem das Objekt instanziiert wird, und vom Speicherort der Initialisierungs Daten.

 

 




