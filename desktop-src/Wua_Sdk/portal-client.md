---
description: Die Windows Update-Agent-API (WUA) ist ein Satz von COM-Schnittstellen, die Systemadministratoren und Programmierern den Zugriff auf Windows Update and Windows Server Update Services (WSUS) ermöglichen.
ms.assetid: 611dc759-e0fc-472e-bdc2-fb952ba74999
title: Windows Update-Agent-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82e7e2c79a707424128082f8f3123cb5fff506a9fc98203ab1fdf8063393310d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117738002"
---
# <a name="windows-update-agent-api"></a>Windows Update-Agent-API

## <a name="purpose"></a>Zweck

Die Windows Update-Agent-API (WUA) ist ein Satz von COM-Schnittstellen, die Systemadministratoren und Programmierern den Zugriff auf Windows Update and [Windows Server Update Services (WSUS) ermöglichen.](/previous-versions/windows/desktop/ms744624(v=vs.85)) Skripts und Programme können geschrieben werden, um zu überprüfen, welche Updates derzeit für einen Computer verfügbar sind. Anschließend können Sie Updates installieren oder deinstallieren.

## <a name="where-applicable"></a>Anwendungsbereich

Systemadministratoren können WUA verwenden, um programmgesteuert zu bestimmen, welche Updates auf einen Computer angewendet werden sollen, diese Updates herunterzuladen und sie dann ohne oder ohne Benutzereingriff zu installieren.

Unabhängige Softwarehersteller (ISV) und Endbenutzerentwickler können WUA-Features in Computerverwaltungs- oder Updateverwaltungssoftware integrieren, um eine nahtlose Betriebsumgebung zu bieten.

## <a name="developer-audience"></a>Entwicklergruppe

Sie können WUA-Anwendungen in mehreren Programmiersprachen schreiben. WUA definiert Schnittstellen und Objekte, auf die über Visual Basic, Visual Basic Scripting Edition (VBScript), JScript und über C und C++ zugegriffen werden kann. Eine Vertrautheit mit der COM-Programmierung ist für den WUA-Programmierer nützlich.

## <a name="run-time-requirements"></a>Laufzeitanforderungen

WUA wird ab xp Windows unterstützt. WUA wird auf dem Server ab Windows Server 2003 unterstützt.

## <a name="in-this-section"></a>In diesem Abschnitt

-   [Verwenden der Windows Update-Agent-API](using-the-windows-update-agent-api.md)
-   [WUA-API-Referenz](windows-update-agent--wua--api-reference.md)

 

 
