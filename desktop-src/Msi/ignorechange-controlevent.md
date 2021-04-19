---
description: Das ignorechange ControlEvent wird vom directorylist-Steuerelement veröffentlicht, wenn der ausgewählte Ordner von einem Verzeichnis in ein anderes Verzeichnis im-Steuerelement geändert wird. Dieses Ereignis sollte in der Tabelle EventMapping erstellt werden.
ms.assetid: 4d3128a1-cbe3-457c-83b5-8f6ec1a7ba29
title: Ignorechange ControlEvent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9db909552e97f29b8ebcd9d58ac8688474788ec0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106362422"
---
# <a name="ignorechange-controlevent"></a>Ignorechange ControlEvent

Das ignorechange ControlEvent wird vom [directorylist-Steuer](directorylist-control.md) Element veröffentlicht, wenn der ausgewählte Ordner von einem Verzeichnis in ein anderes Verzeichnis im-Steuerelement geändert wird. Dieses Ereignis sollte in der [Tabelle EventMapping](eventmapping-table.md)erstellt werden.

Diese ControlEvent erfordert, dass die Benutzeroberfläche auf der [*vollständigen*](f-gly.md) Benutzeroberfläche ausgeführt wird. Dieses Ereignis funktioniert nicht mit einer [*reduzierten Benutzer*](r-gly.md) Oberfläche oder [*grundlegender Benutzeroberfläche*](b-gly.md). Weitere Informationen finden Sie unter [Benutzeroberflächen Ebenen](user-interface-levels.md).

## <a name="published-by"></a>Veröffentlicht von

[Directoren auflisten](directorylist-control.md)

## <a name="argument"></a>Argument

Dieses ControlEvent verwendet kein Argument.

## <a name="action-on-subscribers"></a>Aktion auf Abonnenten

Diese ControlEvent führt keine Aktion für Abonnenten aus.

## <a name="typical-use"></a>Typische Verwendung

Das [directoriycombo-Steuer](directorycombo-control.md) Element verwendet häufig das ignorechange ControlEvent-Steuerelement.

 

 



