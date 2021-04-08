---
title: Erstellen von allgemeinen Steuerelementen
description: In diesem Thema wird beschrieben, wie ein Fenster erstellt wird, das zu einer Fenster Klasse gehört, die in der allgemeinen Steuerelement Bibliothek (Comctl32.dll) definiert ist.
ms.assetid: BCF25606-5B49-43A5-8107-E7220BE3253C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 944e8aa70b3367f1d3a12e4f50032e6677c5d706
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "103949225"
---
# <a name="creating-common-controls"></a>Erstellen von allgemeinen Steuerelementen

In diesem Thema wird beschrieben, wie ein Fenster erstellt wird, das zu einer Fenster Klasse gehört, die in der allgemeinen Steuerelement Bibliothek (Comctl32.dll) definiert ist.


Die häufigsten Steuerelemente gehören zu einer Fenster Klasse, die in der DLL für das allgemeine Steuerelement definiert ist. Die Fenster Klasse und die entsprechende Fenster Prozedur definieren die Eigenschaften, die Darstellung und das Verhalten des Steuer Elements. Um sicherzustellen, dass die DLL des allgemeinen Steuer Elements geladen wird, schließen Sie die [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) -Funktion in Ihre Anwendung ein. Sie erstellen ein gemeinsames Steuerelement, indem Sie den Namen der Fenster Klasse angeben, wenn Sie die [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) -Funktion aufrufen, oder indem Sie den entsprechenden Klassennamen in einer Dialogfeld Vorlage angeben.


Jeder Typ von allgemeinen Steuerelementen verfügt über eine Reihe von Steuerelement Formaten, mit denen Sie die Darstellung und das Verhalten des Steuer Elements variieren können. Die allgemeine Steuerelement Bibliothek umfasst auch einen Satz von Steuerelement Stilen, die auf zwei oder mehr Typen von allgemeinen Steuerelementen angewendet werden. Die allgemeinen Steuerelement Stile werden im Abschnitt " [Stile](common-control-styles.md) " beschrieben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu allgemeinen Steuerelementen](common-controls-intro.md)
</dt> </dl>

 

 