---
description: IgnoreChange ControlEvent wird vom DirectoryList-Steuerelement veröffentlicht, wenn der ausgewählte Ordner von einem Verzeichnis in ein anderes Verzeichnis im -Steuerelement geändert wird. Dieses Ereignis sollte in der EventMapping-Tabelle verfasst werden.
ms.assetid: 4d3128a1-cbe3-457c-83b5-8f6ec1a7ba29
title: IgnoreChange ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8efc2750c4d1e2bd85f7c31348f507917f828725de95658095e964b22a110a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118634458"
---
# <a name="ignorechange-controlevent"></a>IgnoreChange ControlEvent

IgnoreChange ControlEvent wird vom [DirectoryList-Steuerelement](directorylist-control.md) veröffentlicht, wenn der ausgewählte Ordner von einem Verzeichnis in ein anderes Verzeichnis im -Steuerelement geändert wird. Dieses Ereignis sollte in der [EventMapping-Tabelle verfasst werden.](eventmapping-table.md)

Für dieses ControlEvent muss die Benutzeroberfläche auf der vollständigen [*Benutzeroberflächenebene ausgeführt*](f-gly.md) werden. Dieses Ereignis funktioniert nicht mit einer reduzierten [*Benutzeroberfläche oder*](r-gly.md) einer [*einfachen Benutzeroberfläche.*](b-gly.md) Weitere Informationen finden Sie unter [Benutzeroberfläche Levels](user-interface-levels.md).

## <a name="published-by"></a>Veröffentlicht von

[DirectoryList](directorylist-control.md)

## <a name="argument"></a>Argument

Dieses ControlEvent verwendet kein Argument.

## <a name="action-on-subscribers"></a>Aktion auf Abonnenten

Dieses ControlEvent führt keine Aktion auf Abonnenten aus.

## <a name="typical-use"></a>Typische Verwendung

Das [DirectoryCombo-Steuerelement](directorycombo-control.md) verwendet häufig ignoreChange ControlEvent.

 

 



