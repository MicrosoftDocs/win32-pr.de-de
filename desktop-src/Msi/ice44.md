---
description: ICE44 überprüft, ob newDialog, SpawnDialog und SpawnWaitDialog ControlEvents auf gültige Dialogfelder in der Tabelle Dialog verweisen.
ms.assetid: 401bae25-a361-45f6-af3f-0f31be463c84
title: ICE44
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ee7bb074ec2dcc395cdf17750e2ab1b0364026e0f949c9b9e3f2589a8b59261
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119581010"
---
# <a name="ice44"></a>ICE44

ICE44 überprüft, ob [newDialog,](newdialog-controlevent.md) [SpawnDialog](spawndialog-controlevent.md)und [SpawnWaitDialog](spawnwaitdialog-controlevent.md) ControlEvents auf gültige Dialogfelder in der [Dialogtabelle verweisen.](dialog-table.md)

## <a name="result"></a>Ergebnis

ICE44 gibt eine Fehlermeldung aus, wenn es ein Dialogsteuerungsereignis gibt, das nicht auf ein dialogfeld verweist, das in der Tabelle Dialog aufgeführt ist.

## <a name="example"></a>Beispiel

ICE44 würde die folgenden Fehler für das gezeigte Beispiel melden.



| ICE44-Fehler                                                                                                                               | Beschreibung                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Control Event for Control 'Dialog1'." (Steuerelementereignis für Steuerelement "Dialog1".) Control1' ist vom Typ SpawnDialog, aber das Argument Dialog2 ist kein gültiger Eintrag in der Dialogtabelle. | Es gibt eine SpawnDialog-, SpawnWaitDialog- oder NewDialog-Aktion, die über ein Argument verfügt, das nicht auf ein Dialogfeld in der Tabelle Dialog verweisen kann. Um diesen Fehler zu beheben, fügen Sie ein Argument hinzu, das ein Schlüssel in der Dialogtabelle ist.<br/> |



 

[Dialogtabelle](dialog-table.md) (partiell)



| Dialog  | Titel |
|---------|-------|
| Dialog1 |       |



 

[ControlEvent-Tabelle](controlevent-table.md) (partiell)



| Dialog\_ | Steuerelement\_ | Typ        | Argument |
|----------|-----------|-------------|----------|
| Dialog1  | Control1  | SpawnDialog | Dialog2  |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ICE-Referenz](ice-reference.md)
</dt> </dl>

 

 




