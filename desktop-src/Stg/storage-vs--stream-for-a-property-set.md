---
title: Storage und Streamen von Objekten für einen Eigenschaftensatz
description: Der Programmierer gibt an, ob ein Eigenschaftensatz in einem Speicher oder Stream gespeichert wird, wenn der Eigenschaftensatz erstellt wird.
ms.assetid: d0ca649a-d405-4c34-af02-9c2ca8b2790e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e63ff148a72342da4cf5a6d8e1d59feab5c9b5b6fcbdf8a413069413cdb1e63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119661840"
---
# <a name="storage-and-stream-objects-for-a-property-set"></a>Storage und Streamen von Objekten für einen Eigenschaftensatz

Der Programmierer gibt an, ob ein Eigenschaftensatz in einem Speicher oder Stream gespeichert wird, wenn der Eigenschaftensatz erstellt wird. Der PROPSETFLAG \_ NONSIMPLE-Enumerationswert, der im *grfFlags-Parameter* an die [**IPropertySetStorage::Create-Methode**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) übergeben wird, gibt dies an. Das Festlegen des Orts, an dem der Eigenschaftensatz gespeichert ist, stellt die richtigen Anwendungssteuerelemente bereit, um über die [**IPropertySetStorage-Schnittstelle**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) vollständig mit dem COM-Eigenschaftensatz zu zusammenarbeiten.

Wenn das PROPSETFLAG NONSIMPLE-Flag festgelegt ist, wird der Eigenschaftensatz in einem Speicherobjekt gespeichert, und es können nicht einfache Eigenschaftswerte \_ in das Flag geschrieben werden. Nicht einfache Werte enthalten Werte mit einem **VARTYPE** von VT \_ STORAGE, VT \_ STREAM, VT \_ STORED OBJECT oder \_ VT \_ STREAMED \_ OBJECT. Weitere Informationen zu **VARTYPE-Werten** und deren Verwendung finden Sie in der [**PROPVARIANT-Struktur.**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)

Wenn das PROPSETFLAG NONSIMPLE-Flag nicht festgelegt ist, können nur einfache Werte \_ in den Eigenschaftensatz geschrieben werden.

Im Speicherobjekt eines nicht einfachen Eigenschaftensets wird ein Stream namens Contents erstellt. Dies ist der primäre Stream des Eigenschaftensets und enthält alle einfachen Eigenschaftswerte. Nicht einfache Eigenschaftswerte (Streams und Speicher) werden unter dem Hauptspeicherobjekt der Eigenschaft gespeichert, die als Unterstreams und Speicher festgelegt ist. Das heißt, diese nicht einfachen Werte werden als gleichgeordnete Elemente im Contents-Stream gespeichert. Der Name der gleichgeordneten Streams und Speicher wird durch die Implementierung bestimmt und ähnlich wie eine einfache Zeichenfolgeneigenschaft im Contents-Stream gespeichert.

 

 