---
description: Das Medien Streaming-Terminal (MST) ist ein dynamisches Terminal, das auf der Verwendung von DirectShow-Filtern basiert. Ein msp, der mit den TAPI 3-MSP-Basisklassen geschrieben wurde, integriert eine MST, aber MSP-Autoren können diese ohne die Basisklassen implementieren.
ms.assetid: 21015c33-2ad1-4472-b346-167953d06a21
title: Medien Streaming-Terminal (MST)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2afb9bb4b97d0e741aec96454b187beefe2d21eb
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "103961156"
---
# <a name="media-streaming-terminal-mst"></a>Medien Streaming-Terminal (MST)

Das Medien Streaming-Terminal (MST) ist ein dynamisches Terminal, das auf der Verwendung von DirectShow-Filtern basiert. Ein msp, der mit den [TAPI 3-MSP-Basisklassen](tapi-3-msp-base-classes.md) geschrieben wurde, integriert eine MST, aber MSP-Autoren können diese ohne die Basisklassen implementieren.

Um die MST-Erstellung aufzurufen, ruft eine Anwendung [**itterminalsupport:: | ateterminal**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-createterminal) mithilfe von *pterminalclass* auf, die auf CLSID \_ mediastreamterminal festgelegt ist.

Die Schnittstellen [**itammediaformat**](/windows/win32/api/tapi3/nn-tapi3-itammediaformat) und [**itzugenorproperties**](/windows/win32/api/tapi3/nn-tapi3-itallocatorproperties) werden dann im Terminal verfügbar gemacht, sodass eine Anwendung die Streamingleistung optimieren kann. Diese Schnittstellen werden in Tapi3. h deklariert.

Die Implementierung und Verwendung eines MST erfordert Vertrautheit mit DirectShow-Filtern und der Filter Diagramm Verwaltung. Weitere Informationen finden Sie im DirectShow-Material unter dem Grafik-und Multimedia Services-Knoten des Platform Software Development Kit (SDK). Der multimediastreamingverweis ist besonders nützlich für MSP-Autoren.

 

 
