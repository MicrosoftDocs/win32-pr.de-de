---
title: Speicher-und Streamobjekte für einen Eigenschaften Satz
description: Der Programmierer gibt an, ob ein Eigenschaften Satz in einem Speicher oder in einem Stream gespeichert wird, wenn der Eigenschaften Satz erstellt wird.
ms.assetid: d0ca649a-d405-4c34-af02-9c2ca8b2790e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4ebd5d03c3b17e02aa47a7a859576b4cc04607a
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "104039763"
---
# <a name="storage-and-stream-objects-for-a-property-set"></a>Speicher-und Streamobjekte für einen Eigenschaften Satz

Der Programmierer gibt an, ob ein Eigenschaften Satz in einem Speicher oder in einem Stream gespeichert wird, wenn der Eigenschaften Satz erstellt wird. Der nicht einfache propsetflag- \_ Enumerationswert, der im *grfFlags* -Parameter an die [**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) -Methode übergeben wird, gibt dies an. Die Einstellung, in der der Eigenschaften Satz gespeichert wird, bietet geeignete Anwendungs Steuerelemente, um die [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) -Schnittstelle vollständig mit dem com-Eigenschaften Satz zu interagieren.

Wenn das Flag propsetflag \_ nicht einfache festgelegt ist, wird der Eigenschaften Satz in einem Speicher Objekt gespeichert, und es können nicht einfache Eigenschaftswerte in das Flag geschrieben werden. Nicht einfache Werte enthalten Werte mit dem **VarType** -Wert von VT \_ Storage, VT \_ Stream, einem gespeicherten VT- \_ \_ Objekt oder einem VT- \_ Streaming- \_ Objekt. Weitere Informationen zu **VarType** -Werten und deren Verwendung finden Sie in der [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) -Struktur.

Wenn das nonsimple-Flag propsetflag \_ nicht festgelegt ist, können nur einfache Werte in den Eigenschaften Satz geschrieben werden.

Im Speicher Objekt eines nicht einfachen Eigenschaften Satzes wird ein Stream mit dem Namen "Content" erstellt. Dies ist der primäre Stream des Eigenschaften Satzes, der alle einfachen Eigenschaftswerte enthält. Nicht einfache Eigenschaftswerte (Streams und Speicher) werden unter dem Hauptspeicher Objekt der Eigenschaft gespeichert, die als Substreams und Speicherplatz festgelegt ist. Das heißt, dass diese nicht einfachen Werte als gleich geordnete Elemente im Inhaltsstream gespeichert werden. Der Name der gleich geordneten Streams und Speicher wird von der-Implementierung bestimmt und im Inhaltsstream gespeichert, ähnlich der Art, wie eine einfache Zeichen folgen Eigenschaft gespeichert wird.

 

 