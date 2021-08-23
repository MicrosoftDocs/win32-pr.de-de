---
description: Sie können das InkPicture-Steuerelement verwenden, um in Microsoft Windows 2000, Windows Server 2003 und Nicht-Tablet PC-Editionen von Windows XP zu rendern. Sie können das Steuerelement jedoch nicht zum Eingeben von Ink auf diesen Betriebssystemen verwenden.
ms.assetid: e5d00b0f-0a4f-4ea2-ae63-dfb6bc8c2caf
title: Verwenden von InkPicture in früheren Versionen Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52423e8eb3e4c7f59da7a7caac299428dd8efcdce2192819444bfe91070f10b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119091359"
---
# <a name="using-inkpicture-on-earlier-versions-of-windows"></a>Verwenden von InkPicture in früheren Versionen Windows

Sie können das [InkPicture-Steuerelement](inkpicture-control.md) verwenden, um in Microsoft Windows 2000, Windows Server 2003 und Nicht-Tablet PC-Editionen von Windows XP zu rendern. Sie können das Steuerelement jedoch nicht zum Eingeben von Ink auf diesen Betriebssystemen verwenden.

Die [**InkEnabled-Eigenschaft**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_inkenabled) des Steuerelements ist auf **FALSE** festgelegt, und der Versuch, die Eigenschaft zu ändern, hat keine Auswirkungen. Sie können anderen Eigenschaften Werte zuweisen und Frei- programmgesteuert bearbeiten, aber Sie können das -Steuerelement nicht verwenden, um Freiknipsen zu erfassen.

 

 



