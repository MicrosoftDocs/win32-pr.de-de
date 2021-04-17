---
description: Die CurrentDomain-Eigenschaft ruft die DVD-Domäne ab, in der sich das mswebdvd-Objekt befindet.
ms.assetid: 9d545438-9a3d-4c57-a3df-5e75af2e4d1b
title: CurrentDomain (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ead6d61cd622fceac2a4d133a0297892992e763a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481862"
---
# <a name="currentdomain-property"></a>CurrentDomain (Eigenschaft)

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die- `CurrentDomain` Eigenschaft ruft die DVD-Domäne ab, in der sich das mswebdvd-Objekt befindet.

``` syntax
[ iDomain = ] MSWebDVD.CurrentDomain
```

## <a name="return-value"></a>Rückgabewert

Gibt einen ganzzahligen Wert zurück, der die aktuelle Domäne darstellt.

## <a name="remarks"></a>Bemerkungen

Die möglichen Werte der-Eigenschaft sind:



| Wert | BESCHREIBUNG          |
|-------|----------------------|
| 1     | Zuerst abspielen           |
| 2     | Video-Manager-Menü   |
| 3     | Menü "Video Titel Satz" |
| 4     | Titel                |
| 5     | Stop                 |



 

Mit dieser Methode können Sie sicherstellen, dass sich der DVD-Navigator in einer gültigen Domäne für die aufzurufende Methode befindet. Überprüfen Sie z. b. vor dem Aufrufen von [**playtitle**](playtitle-method.md)die- `CurrentDomain` Eigenschaft, um sicherzustellen, dass sich der DVD-Navigator nicht in der "beendet" oder "erste Wiedergabe"

 

 



