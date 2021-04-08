---
description: Mit der Device Power API können Sie leicht feststellen, welche Geräte das System aus dem Ruhezustand reaktivieren können und in welchen Ruhe Zuständen diese Geräte das Erwachen unterstützen. Weitere Informationen zu Ruhe Zuständen finden Sie unter System Energiezustände.
ms.assetid: aaa776e5-3fc2-41bd-a805-6c09ef73807b
title: Geräte Energie Verwaltung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0982b7de23f7b7d8cf39686c854d64f284d1ce2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959746"
---
# <a name="device-power-management"></a>Geräte Energie Verwaltung

Mit der Device Power API können Sie leicht feststellen, welche Geräte das System aus dem Ruhezustand reaktivieren können und in welchen Ruhe Zuständen diese Geräte das Erwachen unterstützen. Weitere Informationen zu Ruhe Zuständen finden Sie unter [System Energiezustände](system-power-states.md).

Die [**devicepowerenumdevices**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowerenumdevices) -Funktion kann verwendet werden, um die Geräteliste nach Geräten zu durchsuchen, die mit den angegebenen Kriterien übereinstimmen. Die Kriterien können die Fähigkeit des Geräts enthalten, einen Systemstatus zu unterstützen oder diesen Zustand zu aktivieren. Zurzeit werden unterstützte Flags in "Winnt. h" und "devpower. h" gefunden.

Die [**devicepowersetdevicestate**](/windows/desktop/api/PowrProf/nf-powrprof-devicepowersetdevicestate) -Funktion aktiviert oder deaktiviert, dass ein angegebenes Gerät das System aus dem Ruhezustand reaktiviert.

Mit der Device Power API können Entwickler eine bessere Benutzer Leistung erzielen, indem Sie dem Benutzer mehr Informationen über das, was das System leistet, und mehr Kontrolle über die Geräte im System geben. Die Geräteleistung ist in Situationen nützlich, in denen der Energieverbrauch wichtig ist, z. b. auf tragbaren Geräten, die unter Batterien ausgeführt werden Beispielsweise ist das Energie Verwaltungs Schema, das auf einem Desktop Computer verwendet wird, möglicherweise nicht das optimale Schema für einen Laptop Computer, sodass der Benutzer bestimmte Geräte vor dem Reaktivieren des Systems deaktivieren möchte. Dadurch können Energie gespart werden, da die deaktivierten Geräte keine Stromversorgung zeichnen, während sich das System im Energiesparmodus befindet.

Ein Beispiel finden Sie unter [Verwenden der Device Power API](using-the-device-power-api.md).

 

 



