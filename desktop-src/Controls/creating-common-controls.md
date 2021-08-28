---
title: Erstellen allgemeiner Steuerelemente
description: In diesem Thema wird beschrieben, wie Sie ein Fenster erstellen, das zu einer Fensterklasse gehört, die in der allgemeinen Steuerelementbibliothek Comctl32.dll definiert ist.
ms.assetid: BCF25606-5B49-43A5-8107-E7220BE3253C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26ddc06def47cef1a34849bbe31bc3871d4c098890bd3ef53830ae6fe7076520
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916340"
---
# <a name="creating-common-controls"></a>Erstellen allgemeiner Steuerelemente

In diesem Thema wird beschrieben, wie Sie ein Fenster erstellen, das zu einer Fensterklasse gehört, die in der allgemeinen Steuerelementbibliothek Comctl32.dll definiert ist.


Die meisten gängigen Steuerelemente gehören zu einer Fensterklasse, die in der allgemeinen Steuerelement-DLL definiert ist. Die Fensterklasse und die entsprechende Fensterprozedur definieren die Eigenschaften, die Darstellung und das Verhalten des Steuerelements. Um sicherzustellen, dass die allgemeine Steuerelement-DLL geladen wird, schließen Sie die [**InitCommonControlsEx-Funktion**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) in Ihre Anwendung ein. Sie erstellen ein allgemeines Steuerelement, indem Sie den Namen der Fensterklasse angeben, wenn Sie die [**CreateWindowEx-Funktion**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) aufrufen, oder indem Sie den entsprechenden Klassennamen in einer Dialogfeldvorlage angeben.


Jeder Typ eines allgemeinen Steuerelements verfügt über eine Reihe von Steuerelementstilen, die Sie verwenden können, um die Darstellung und das Verhalten des Steuerelements zu variieren. Die allgemeine Steuerelementbibliothek enthält auch eine Reihe von Steuerelementstilen, die für zwei oder mehr Typen von allgemeinen Steuerelementen gelten. Die allgemeinen Steuerelementstile werden im Abschnitt [Stile](common-control-styles.md) beschrieben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu allgemeinen Steuerelementen](common-controls-intro.md)
</dt> </dl>

 

 