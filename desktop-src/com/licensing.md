---
title: Lizenzierung
description: Lizenzierung
ms.assetid: a77c0141-62b4-4032-a734-5a55da6a50e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06066365d2cf00a7b5db6d6ca755261e5a9470fa
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730497"
---
# <a name="licensing"></a>Lizenzierung

Um lizenzierte Steuerelemente erfolgreich einzubetten, müssen die ActiveX-Steuerelement Container anstelle von [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) verwenden. Mehrere OLE-Erstellungs-und lade Hilfsfunktionen ([**OLELOAD**](/windows/desktop/api/Ole2/nf-ole2-oleload) und [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)) rufen explizit **IClassFactory** und nicht **IClassFactory2** auf und können daher nicht zum Erstellen oder Laden von lizenzierten ActiveX-Steuerelementen verwendet werden. ActiveX-Steuerelement Container sollten ActiveX-Steuerelemente explizit mithilfe von **IClassFactory2** erstellen und laden.

 

 