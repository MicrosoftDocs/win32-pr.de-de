---
title: Class Factory-Optionen
description: Class Factory-Optionen
ms.assetid: e9e33e07-7628-4c5e-965d-e12a9c1d69c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fab52ea11a0e7e20d10757eb8d6e86577afc35c
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730432"
---
# <a name="class-factory-options"></a>Class Factory-Optionen

Ein ActiveX-Steuerelement muss aufgrund eines COM-Objekts über zugeordneten Servercode verfügen, der das Erstellen von Steuerelementen über [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) unterstützt.

Es ist optional, nicht erforderlich, dass dieses Klassenobjekt auch [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) für die Lizenzierungs Verwaltung unterstützt. Nur die Hersteller, die sich mit der Lizenzierung beschäftigen, müssen den Lizenzierungs Mechanismus von com unterstützen. Anders ausgedrückt: da **IClassFactory2** die einzige Möglichkeit ist, eine Lizenzierung auf com-Ebene zu erreichen, ist diese Schnittstelle für das Klassenobjekt für die Steuerelemente, die lizenziert werden sollen, erforderlich.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Steuerelemente](controls.md)
</dt> </dl>

 

 