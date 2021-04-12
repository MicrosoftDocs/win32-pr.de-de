---
description: Übersicht über teilweise vertrauenswürdige Probleme und die StylusInput-API (Application Programming Interface).
ms.assetid: 32c26632-03f4-4f21-8c67-ebf38b67d251
title: Überlegungen zur teilweisen Vertrauenswürdigkeit für die StylusInput-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ceda5edfb2e4133bb0fcb3d260ff1e13f9fdb521
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217203"
---
# <a name="partial-trust-considerations-for-the-stylusinput-api"></a>Überlegungen zur teilweisen Vertrauenswürdigkeit für die StylusInput-API

Der [**RealTimeStylus**](realtimestylus-class.md) , der den *handle* -Parameter annimmt, erfordert zusätzlich zu den Berechtigungen, die für den Konstruktor erforderlich sind, der den Parameter " *AttachedControl* " annimmt, die Berechtigungen " [UIPermissionWindow. AllWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true) " und " [SecurityPermissionFlag. UnmanagedCode](/previous-versions/windows/) ".

Weitere Informationen zu Sicherheits-und Vertrauensstellungs Problemen finden Sie unter [Sicherheit und Vertrauens](security-and-trust.md)Stellung.

 

 
