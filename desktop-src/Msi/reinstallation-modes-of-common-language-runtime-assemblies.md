---
description: Common Language Runtime-Assemblys, die im globalen Assemblycache installiert sind, müssen in allen Vorkommen der Assembly über identische Dateien verfügen.
ms.assetid: 02b4ad60-d28d-44b8-955f-b367197e69c3
title: Neuinstallations Modi von Common Language Runtime-Assemblys
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8512e4c6e888c7d67b2ca252184fa4f748445fb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353442"
---
# <a name="reinstallation-modes-of-common-language-runtime-assemblies"></a>Neuinstallations Modi von Common Language Runtime-Assemblys

Common Language Runtime-Assemblys, die im globalen Assemblycache installiert sind, müssen in allen Vorkommen der Assembly über identische Dateien verfügen. Dies bedeutet, dass die von " [**msireinstallfeature**](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea) " und " [**msireinstallproduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta) " verwendeten Neuinstallations Modi für reguläre Komponenten und Common Language Runtime Assemblys unterschiedliche Bedeutungen haben müssen. Die folgenden Definitionen der neuinstallationsmodi gelten für Common Language Runtime Assemblys.



| Neuinstallations Modus                  | Bedeutung für Microsoft .NET Komponenten                                                                                              |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| Datei für den erneuten installmode \_ fehlt      | Installieren Sie die Common Language Runtime Komponente, oder installieren Sie Sie neu, falls Sie fehlt oder unvollständig ist.                                         |
| REINSTALLMODE- \_ fileolderversion | Installieren Sie die Common Language Runtime Komponente, oder installieren Sie Sie neu, falls Sie fehlt oder unvollständig ist.                                         |
| REINSTALLMODE- \_ fileequalversion | Installieren Sie die Common Language Runtime Komponente, oder installieren Sie Sie neu, falls Sie fehlt oder unvollständig ist.                                         |
| REINSTALLMODE \_ File Exact        | Installieren Sie die Common Language Runtime Komponente, oder installieren Sie Sie neu, falls Sie fehlt oder unvollständig ist.                                         |
| REINSTALLMODE- \_ Filter       | Installieren Sie die Common Language Runtime Komponente, oder installieren Sie Sie neu, wenn Sie nicht vorhanden ist oder wenn die vorhandene Komponente unvollständig oder beschädigt ist. |
| REINSTALLMODE- \_ filereplace      | Installieren Sie die Common Language Runtime Komponente immer, oder installieren Sie Sie neu.                                                                 |



 

 

 



