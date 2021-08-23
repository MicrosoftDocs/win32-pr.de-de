---
description: Das Media Streaming Terminal (MST) ist ein dynamisches Terminal, das auf der Verwendung von DirectShow-Filtern basiert. Ein MSP, der mit den TAPI 3 MSP-Basisklassen geschrieben wurde, enthält einen MST, aber MSP-Autoren können ihn implementieren, ohne die Basisklassen zu verwenden.
ms.assetid: 21015c33-2ad1-4472-b346-167953d06a21
title: Media Streaming Terminal (MST)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8eeb9ad231c114ca18b4dea0926b861360ab5a359cd9ee8c48fd1c388a941a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002908"
---
# <a name="media-streaming-terminal-mst"></a>Media Streaming Terminal (MST)

Das Media Streaming Terminal (MST) ist ein dynamisches Terminal, das auf der Verwendung von DirectShow-Filtern basiert. Ein MSP, der mit den [TAPI 3 MSP-Basisklassen](tapi-3-msp-base-classes.md) geschrieben wurde, enthält einen MST, aber MSP-Autoren können ihn implementieren, ohne die Basisklassen zu verwenden.

Um die MST-Erstellung aufzurufen, ruft eine Anwendung [**ITTerminalSupport::CreateTerminal**](/windows/win32/api/tapi3if/nf-tapi3if-itterminalsupport-createterminal) auf, indem *pTerminalClass* auf CLSID \_ MediaStreamTerminal festgelegt ist.

Die Schnittstellen [**ITAMMediaFormat**](/windows/win32/api/tapi3/nn-tapi3-itammediaformat) und [**ITAllocatorProperties**](/windows/win32/api/tapi3/nn-tapi3-itallocatorproperties) werden dann im Terminal verfügbar gemacht, sodass eine Anwendung die Streamingleistung optimieren kann. Diese Schnittstellen werden in Tapi3.h deklariert.

Die Implementierung und Verwendung eines MST erfordert Vertrautheit mit DirectShow-Filtern und Filtergraphverwaltung. Weitere Informationen finden Sie im DirectShow-Material unter dem Knoten Grafik- und Multimediadienste des Platform Software Development Kit (SDK). Die Multimediastreamingreferenz ist für MSP-Autoren besonders nützlich.

 

 
