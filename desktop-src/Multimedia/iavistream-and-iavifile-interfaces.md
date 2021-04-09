---
title: Iavistream-und iavifile-Schnittstellen
description: Iavistream-und iavifile-Schnittstellen
ms.assetid: 3ab602da-239f-44ff-b43d-e0c380619d99
keywords:
- Iavistream-Schnittstelle
- Iavifile-Schnittstelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f65cdd72a034f2c380638979e656c84a173331fc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856359"
---
# <a name="iavistream-and-iavifile-interfaces"></a>Iavistream-und iavifile-Schnittstellen

Die [**iavistream**](/windows/desktop/api/Vfw/nn-vfw-iavistream) -und [**iavifile**](/windows/desktop/api/Vfw/nn-vfw-iavifile) -Schnittstellen enthalten die Methoden, die von Datei-und streamhandlern verwendet werden. Der-Datentyp von " **pvistream** " ist ein Zeiger auf ein AVI-Streamobjekt (über die **iavistream** -Schnittstelle), und der Datentyp " **pvifile** " ist ein Zeiger auf ein Objekt vom Typ "AVI" (über die Schnittstelle **iavifile** )

Um einen Objekt Zeiger in C zu erstellen, weisen Sie zunächst Speicherplatz für eine Struktur zu, die groß genug ist, um den Zeiger auf die virtuelle Funktions Tabelle und die anderen Datenmember zu enthalten. Erstellen Sie eine virtuelle Funktions Tabelle für die Methoden für den Typ des Streams, und legen Sie dann den Zeiger auf die virtuelle Funktions Tabelle auf die Adresse der virtuellen Funktions Tabelle fest.

 

 




