---
description: Die msiunpublishassemblyaktion verwaltet die Ankündigung von Common Language Runtime Assemblys und Win32-Assemblys, die entfernt werden.
ms.assetid: 199d72be-bbe1-4777-a913-2e4b92576bfa
title: Msiunpublishassemblyaktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91d398c66781e6e356b110828c56de6f5e616775
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867468"
---
# <a name="msiunpublishassemblies-action"></a>Msiunpublishassemblyaktion

Die msiunpublishassemblyaktion verwaltet die Ankündigung von Common Language Runtime Assemblys und Win32-Assemblys, die entfernt werden. Mit der-Aktion wird die [MsiAssembly-Tabelle](msiassembly-table.md) abgefragt, um zu bestimmen, welche Assemblys angekündigte oder installierte Features aus dem globalen Assemblycache entfernt haben und welche Assemblys eine angekündigte oder installierte übergeordnete Komponente von einem Speicherort entfernt wird, der für eine bestimmte Weitere Informationen finden Sie unter Installieren von Assemblys [im globalen Assemblycache](installation-of-assemblies-to-the-global-assembly-cache.md) und [Installieren von Win32](installation-of-win32-assemblies.md)-Assemblys.

Auf Systemen, auf denen Windows XP und höher ausgeführt wird, können Windows Installer Win32-Assemblys [als parallele](side-by-side-assemblies.md)Assemblys installieren. Weitere Informationen finden Sie unter Informationen [zu isolierten Anwendungen und](../sbscs/about-isolated-applications-and-side-by-side-assemblies.md)parallelen Assemblys.

## <a name="sequence-restrictions"></a>Sequenz Einschränkungen

Die msiunpublishassemblyaktion muss nach der [InstallInitialize-Aktion](installinitialize-action.md) in der [InstallExecuteSequence-Tabelle](installexecutesequence-table.md)erfolgen.

## <a name="actiondata-messages"></a>Aktions Daten Meldungen



| Feld | Beschreibung der Aktions Daten |
|-------|----------------------------|
| \[1\] | Anwendungskontext.       |
| \[2\] | AssemblyName.             |



 

## <a name="remarks"></a>Bemerkungen

Die [msipublishassemblyaktion](msipublishassemblies-action.md) verwaltet die Ankündigung von Assemblys, die angekündigt oder installiert werden.

 

 
