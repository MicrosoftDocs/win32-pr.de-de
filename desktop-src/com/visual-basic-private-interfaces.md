---
title: Private Schnittstellen Visual Basic
description: Private Schnittstellen Visual Basic
ms.assetid: 782e5d87-680e-4d0c-b1e6-cf97d1a37ce5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5af32f46c02b9b76cdf3dd83e9a22a028aaa88d7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037608"
---
# <a name="visual-basic-private-interfaces"></a>Private Schnittstellen Visual Basic

Hier werden zwei von Visual Basic implementierte Schnittstellen für Komponenten Kategorien identifiziert. Es ist nicht zu erwarten, dass Steuerelemente diese Kategorien benötigen, da Steuerelemente eine Alternative Funktionalität anbieten können, wenn diese nicht verfügbar sind.

Mit der [**IVBFormat**](/windows/desktop/api/VbInterf/nn-vbinterf-ivbformat) -Schnittstelle können Steuerelemente beim Formatieren von Daten besser in die Visual Basic Umgebung integriert werden.

CATID-{02496840-3ac4-11CF-87b9-00aa006c8166} CATID \_ vbformat

Die [**IVBGetControl**](/windows/desktop/api/VbInterf/nn-vbinterf-ivbgetcontrol) -Schnittstelle ermöglicht es einem Steuerelement, andere Steuerelemente auf dem VB-Formular aufzuzählen.

CATID-{02496841-3ac4-11CF-87b9-00aa006c8166} CATID \_ vbgetcontrol

Zwei weitere private Schnittstellen, [**IGetVBAObject**](/windows/desktop/api/VbInterf/nn-vbinterf-igetvbaobject) und [**igetoleobject**](/windows/desktop/api/VbInterf/nn-vbinterf-igetoleobject), werden hier beschrieben, auch wenn Sie keine Komponenten Kategorien definieren. Die Verwendung dieser vier Schnittstellen ist nicht empfehlenswert, da Sie von anderen Containern als Visual Basic nicht unterstützt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Komponentenkategorien](component-categories.md)
</dt> </dl>

 

 




