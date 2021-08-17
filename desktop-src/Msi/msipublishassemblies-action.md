---
description: Die MsiPublishAssemblies-Aktion verwaltet die Ankündigung von Common Language Runtime-Assemblys und Win32-Assemblys.
ms.assetid: 4bc67f43-7a7e-4bd3-aa83-610b46a54e11
title: MsiPublishAssemblies-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 524175a957249a48f7c72409ad7b4c55b31f642753db11875a9567ef35a2acf8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117804190"
---
# <a name="msipublishassemblies-action"></a>MsiPublishAssemblies-Aktion

Die MsiPublishAssemblies-Aktion verwaltet die Ankündigung von Common Language Runtime-Assemblys und Win32-Assemblys. Die Aktion fragt die [MsiAssembly-Tabelle](msiassembly-table.md) ab, um zu bestimmen, welche Assemblys Features im globalen Assemblycache angekündigt oder installiert werden und welche Assemblys eine übergeordnete Komponente an einem speicherort isolierten Speicherort für eine bestimmte Anwendung angekündigt oder installiert haben. Weitere Informationen finden Sie unter [Installation von Assemblys im globalen Assemblycache](installation-of-assemblies-to-the-global-assembly-cache.md) und [Installation von Win32-Assemblys.](installation-of-win32-assemblies.md)

Auf Systemen mit Microsoft Windows XP und höher kann Windows Installer Win32-Assemblys als [nebenseitige Assemblys](side-by-side-assemblies.md)installieren. Weitere Informationen finden Sie unter [Informationen zu isolierten Anwendungen und nebeneinander angezeigten Assemblys.](../sbscs/about-isolated-applications-and-side-by-side-assemblies.md)

## <a name="sequence-restrictions"></a>Sequenzeinschränkungen

Die MsiPublishAssemblies-Aktion muss nach der [InstallInitialize-Aktion](installinitialize-action.md) in der [Tabelle InstallExecuteSequence](installexecutesequence-table.md) oder der [AdvtExecuteSequence-Tabelle erfolgen.](advtexecutesequence-table.md)

## <a name="actiondata-messages"></a>ActionData-Nachrichten



| Feld | Beschreibung der Aktionsdaten |
|-------|----------------------------|
| \[1\] | Anwendungskontext.       |
| \[2\] | Name der Assembly.             |



 

## <a name="remarks"></a>Hinweise

Weitere Informationen finden Sie unter [Assemblys](assemblies.md).

Die [MsiUnpublishAssemblies-Aktion](msiunpublishassemblies-action.md) verwaltet die Ankündigung von Assemblys, die entfernt werden.

 

 
