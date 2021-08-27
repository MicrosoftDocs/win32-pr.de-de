---
description: Die MsiUnpublishAssemblies-Aktion verwaltet die Ankündigung von Common Language Runtime-Assemblys und Win32-Assemblys, die entfernt werden.
ms.assetid: 199d72be-bbe1-4777-a913-2e4b92576bfa
title: MsiUnpublishAssemblies-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f640338e13f53b115ca3b93aa2a63987efb5aa7cf053d4c8a59d8d20d0f7e3fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118943897"
---
# <a name="msiunpublishassemblies-action"></a>MsiUnpublishAssemblies-Aktion

Die MsiUnpublishAssemblies-Aktion verwaltet die Ankündigung von Common Language Runtime-Assemblys und Win32-Assemblys, die entfernt werden. Die Aktion fragt die [MsiAssembly-Tabelle](msiassembly-table.md) ab, um zu bestimmen, welche Assemblys Angekündigte oder installierte Features aus dem globalen Assemblycache entfernt haben und welche Assemblys eine angekündigte oder installierte übergeordnete Komponente von einem Speicherort entfernt haben, der für eine bestimmte Anwendung isoliert ist. Weitere Informationen finden Sie unter [Installation von Assemblys im globalen Assemblycache](installation-of-assemblies-to-the-global-assembly-cache.md) und [Installation von Win32-Assemblys.](installation-of-win32-assemblies.md)

Auf Systemen, auf denen Windows XP und höher ausgeführt wird, kann Windows Installer Win32-Assemblys als [nebenseitige Assemblys](side-by-side-assemblies.md)installieren. Weitere Informationen finden Sie unter [Informationen zu isolierten Anwendungen und nebeneinander angezeigten Assemblys.](../sbscs/about-isolated-applications-and-side-by-side-assemblies.md)

## <a name="sequence-restrictions"></a>Sequenzeinschränkungen

Die MsiUnpublishAssemblies-Aktion muss nach der [InstallInitialize-Aktion](installinitialize-action.md) in der [Tabelle InstallExecuteSequence erfolgen.](installexecutesequence-table.md)

## <a name="actiondata-messages"></a>ActionData-Nachrichten



| Feld | Beschreibung der Aktionsdaten |
|-------|----------------------------|
| \[1\] | Anwendungskontext.       |
| \[2\] | Name der Assembly.             |



 

## <a name="remarks"></a>Hinweise

Die [MsiPublishAssemblies-Aktion](msipublishassemblies-action.md) verwaltet die Ankündigung von Assemblys, die angekündigt oder installiert werden.

 

 
