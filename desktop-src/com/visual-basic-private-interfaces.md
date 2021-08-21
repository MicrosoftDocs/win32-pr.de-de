---
title: Visual Basic Private Schnittstellen
description: Visual Basic Private Schnittstellen
ms.assetid: 782e5d87-680e-4d0c-b1e6-cf97d1a37ce5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd69e70d351245ebafa62d521a133726be568a0437f4e04ece4ef761535f4625
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047708"
---
# <a name="visual-basic-private-interfaces"></a>Visual Basic Private Schnittstellen

Zwei Schnittstellen, die von Visual Basic implementiert werden, werden hier für Komponentenkategorien identifiziert. Es ist nicht zu erwarten, dass Steuerelemente diese Kategorien erfordern, da Es möglich ist, dass Steuerelemente alternative Funktionen anbieten, wenn diese nicht verfügbar sind.

Mit der [**IVBFormat-Schnittstelle**](/windows/desktop/api/VbInterf/nn-vbinterf-ivbformat) können Steuerelemente beim Formatieren von Daten besser in die Visual Basic-Umgebung integriert werden.

CATID : {02496840-3AC4-11cf-87B9-00AA006C8166} CATID \_ VBFormat

Die [**IVBGetControl-Schnittstelle**](/windows/desktop/api/VbInterf/nn-vbinterf-ivbgetcontrol) ermöglicht einem Steuerelement das Aufzählen anderer Steuerelemente auf dem VB Formular.

CATID : {02496841-3AC4-11cf-87B9-00AA006C8166} CATID \_ VBGetControl

Zwei zusätzliche private Schnittstellen, [**IGetVBAObject**](/windows/desktop/api/VbInterf/nn-vbinterf-igetvbaobject) und [**IGetOleObject,**](/windows/desktop/api/VbInterf/nn-vbinterf-igetoleobject)werden hier beschrieben, obwohl sie keine Komponentenkategorien definieren. Die Verwendung dieser vier Schnittstellen wird nicht empfohlen, da sie von Containern außer Visual Basic nicht unterstützt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Komponentenkategorien](component-categories.md)
</dt> </dl>

 

 




