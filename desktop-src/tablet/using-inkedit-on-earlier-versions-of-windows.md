---
description: Aufgrund fehlender erkenungen bei nicht Tablet PC-Editionen von Microsoft Windows XP können Sie InkEdit nicht zum Rendering von Freihand auf Windows 2000-, Windows Server 2003-und nicht-Tablet PC-Editionen von Windows XP verwenden, und Sie können das Steuerelement nicht zum Eingeben von frei Hand Eingaben für diese Betriebssysteme verwenden.
ms.assetid: eb80ff91-5c09-43d1-afd4-6391097000c1
title: Verwenden von InkEdit unter früheren Versionen von Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08343b3d379a3f45985b1f586254e7a370998f15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345089"
---
# <a name="using-inkedit-on-earlier-versions-of-windows"></a>Verwenden von InkEdit unter früheren Versionen von Windows

Aufgrund fehlender erkenungen bei nicht Tablet PC-Editionen von Microsoft Windows XP können Sie [InkEdit](inkedit-control.md) nicht zum Rendering von Freihand auf Windows 2000-, Windows Server 2003-und nicht-Tablet PC-Editionen von Windows XP verwenden, und Sie können das Steuerelement nicht zum Eingeben von frei Hand Eingaben für diese Betriebssysteme verwenden.

Die [**InkMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode) -Eigenschaft des Steuer Elements ist auf **deaktiviert** festgelegt (IEM ist für C++**\_ deaktiviert** ), und der Versuch, die Eigenschaft zu ändern, hat keine Auswirkungen. Sie können anderen Eigenschaften Werte zuweisen und Freihand in andere Anwendungen kopieren und einfügen, aber Sie können das Steuerelement nicht verwenden, um Gesten anzunehmen oder frei Hand Eingaben zu sammeln.

 

 



