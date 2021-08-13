---
description: Übersicht über teilweise vertrauenswürdige Probleme und die StylusInput-Anwendungsprogrammierschnittstelle (API).
ms.assetid: 32c26632-03f4-4f21-8c67-ebf38b67d251
title: Überlegungen zur teilweisen Vertrauenswürdigkeit für die StylusInput-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 596e8b50692ae09e9fbaf73f9254afbec8f29d6481a2dc3e27727beb27546441
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449350"
---
# <a name="partial-trust-considerations-for-the-stylusinput-api"></a>Überlegungen zur teilweisen Vertrauenswürdigkeit für die StylusInput-API

Für [**den RealTimeStylus,**](realtimestylus-class.md) der den *handle-Parameter* akzeptiert, sind die [Berechtigungen UIPermissionWindow.AllWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true) und [SecurityPermissionFlag.UnmanagedCode](/previous-versions/windows/) zusätzlich zu den Berechtigungen erforderlich, die vom Konstruktor benötigt werden, der den *attachedControl-Parameter* akzeptiert.

Weitere Informationen zu Sicherheits- und Vertrauensproblemen finden Sie unter [Sicherheit und Vertrauenswürdigkeit.](security-and-trust.md)

 

 
