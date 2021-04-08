---
description: Die Windows Update Agent-API (WUA) ist ein Satz von COM-Schnittstellen, mit denen Systemadministratoren und Programmierer auf Windows Update und Windows Server Update Services (WSUS) zugreifen können.
ms.assetid: 611dc759-e0fc-472e-bdc2-fb952ba74999
title: Windows Update-Agent-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19c34cb76619c9739c84e650a32590fdc4f61022
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750000"
---
# <a name="windows-update-agent-api"></a>Windows Update-Agent-API

## <a name="purpose"></a>Zweck

Die Windows Update Agent-API (WUA) ist ein Satz von COM-Schnittstellen, mit denen Systemadministratoren und Programmierer auf Windows Update und [Windows Server Update Services (WSUS)](/previous-versions/windows/desktop/ms744624(v=vs.85))zugreifen können. Skripts und Programme können geschrieben werden, um zu überprüfen, welche Updates derzeit für einen Computer verfügbar sind. Anschließend können Sie Updates installieren oder deinstallieren.

## <a name="where-applicable"></a>Anwendungsbereich

System Administratoren können WUA verwenden, um Programm gesteuert zu ermitteln, welche Updates auf einen Computer angewendet werden sollen, diese Updates herunterzuladen und dann mit geringem oder ohne Benutzereingriff zu installieren.

Unabhängige Softwareanbieter (Independent Softwareanbieters, ISV) und Endbenutzer Entwickler können WUA-Features in die Computer Verwaltung oder Update Verwaltungssoftware integrieren, um eine nahtlose Betriebsumgebung bereitzustellen.

## <a name="developer-audience"></a>Entwicklergruppe

WUA-Anwendungen können in mehreren Programmiersprachen geschrieben werden. WUA definiert Schnittstellen und Objekte, auf die von Visual Basic, Visual Basic Scripting Edition (VBScript), JScript und von C und C++ aus zugegriffen werden kann. Eine Vertrautheit mit der com-Programmierung ist für den WUA-Programmierer nützlich.

## <a name="run-time-requirements"></a>Laufzeitanforderungen

WUA wird ab Windows XP unterstützt. WUA wird auf dem Server ab Windows Server 2003 unterstützt.

## <a name="in-this-section"></a>In diesem Abschnitt

-   [Verwenden der Windows Update-Agent-API](using-the-windows-update-agent-api.md)
-   [WUA-API-Referenz](windows-update-agent--wua--api-reference.md)

 

 
