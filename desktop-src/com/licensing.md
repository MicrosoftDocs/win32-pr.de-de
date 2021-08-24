---
title: Lizenzierung
description: Lizenzierung
ms.assetid: a77c0141-62b4-4032-a734-5a55da6a50e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3058bd6bb543f2f3fc97f2e6a851b456638128c6e731050237aa0d36b12d681
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119567740"
---
# <a name="licensing"></a>Lizenzierung

Um lizenzierte Steuerelemente erfolgreich einzubetten, müssen ActiveX Steuerelementcontainer [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) anstelle von [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory)verwenden. Mehrere Hilfsfunktionen zum Erstellen und Laden von OLE ([**OleLoad**](/windows/desktop/api/Ole2/nf-ole2-oleload) und [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)) rufen **IClassFactory** explizit und nicht **IClassFactory2** auf und können daher nicht zum Erstellen oder Laden lizenzierter ActiveX-Steuerelemente verwendet werden. ActiveX Steuerelementcontainer sollten ActiveX Controls explizit mithilfe von **IClassFactory2** erstellen und laden.

 

 