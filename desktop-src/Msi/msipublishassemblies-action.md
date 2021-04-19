---
description: Die msipublishassemblyaktion verwaltet die Ankündigung von Common Language Runtime Assemblys und Win32-Assemblys.
ms.assetid: 4bc67f43-7a7e-4bd3-aa83-610b46a54e11
title: Msipublishassemblyaktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c24e1787aeb87cf00eb82aefab375771c7c1ddc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350137"
---
# <a name="msipublishassemblies-action"></a>Msipublishassemblyaktion

Die msipublishassemblyaktion verwaltet die Ankündigung von Common Language Runtime Assemblys und Win32-Assemblys. Mit der-Aktion wird die [MsiAssembly-Tabelle](msiassembly-table.md) abgefragt, um zu bestimmen, welche Assemblys im globalen Assemblycache angekündigt oder installiert werden und welche Assemblys über eine übergeordnete Komponente verfügen, die für eine bestimmte Anwendung isoliert ist. Weitere Informationen finden Sie unter Installieren von Assemblys [im globalen Assemblycache](installation-of-assemblies-to-the-global-assembly-cache.md) und [Installieren von Win32](installation-of-win32-assemblies.md)-Assemblys.

Auf [Systemen mit Microsoft](side-by-side-assemblies.md)Windows XP und höher können Windows Installer Win32-Assemblys als parallele Assemblys installieren. Weitere Informationen finden Sie unter Informationen [zu isolierten Anwendungen und](../sbscs/about-isolated-applications-and-side-by-side-assemblies.md)parallelen Assemblys.

## <a name="sequence-restrictions"></a>Sequenz Einschränkungen

Die msipublishassemblyaktion muss nach der [InstallInitialize-Aktion](installinitialize-action.md) in der [InstallExecuteSequence-Tabelle](installexecutesequence-table.md) oder der [AdvtExecuteSequence-Tabelle](advtexecutesequence-table.md)erfolgen.

## <a name="actiondata-messages"></a>Aktions Daten Meldungen



| Feld | Beschreibung der Aktions Daten |
|-------|----------------------------|
| \[1\] | Anwendungskontext.       |
| \[2\] | AssemblyName.             |



 

## <a name="remarks"></a>Bemerkungen

Weitere Informationen finden Sie unter [](assemblies.md)Assemblys.

Die [msiunpublishassemblyaktion](msiunpublishassemblies-action.md) verwaltet die Ankündigung der zu entfernenden Assemblys.

 

 
