---
description: Erfahren Sie Windows Installer-Konzepte, die mit dem Buchstaben D beginnen, z. B. Datenbankfunktion und Deltapatch.
ms.assetid: d6dd73e7-657f-4f71-8e9b-70369cb21972
title: D (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9a2e1099386a2da176eb899c7974c60244636f6da1384543bde4975ba3a18c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119289670"
---
# <a name="d-windows-installer"></a>D (Windows Installer)

[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) D [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) T [](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z

<dl> <dt>

<span id="_msi_database_function_gly"></span><span id="_MSI_DATABASE_FUNCTION_GLY"></span>**Database-Funktion**
</dt> <dd>

Greifen Sie auf die Installer-Datenbank zu. Diese Funktionen werden in [](i-gly.md) erster Linie für die Verwendung durch Erstellungstools für Installerpakete bereitgestellt und sind nicht für den Aufruf von Installationsdiensten vorgesehen. Weitere Informationen finden Sie unter [Database Functions (Datenbankfunktionen)](database-functions.md) und [in der Installer Function Reference (Referenz zur Installerfunktion).](installer-function-reference.md)

</dd> <dt>

<span id="_msi_database_handle_gly"></span><span id="_MSI_DATABASE_HANDLE_GLY"></span>**Datenbankhand handle**
</dt> <dd>

Erforderlich für die Arbeit mit einer Datenbank. Weitere Informationen finden Sie unter [Abrufen eines Datenbankhandpunkts.](obtaining-a-database-handle.md)

</dd> <dt>

<span id="setup.delta_patch_gly"></span><span id="SETUP.DELTA_PATCH_GLY"></span>**Deltapatch**
</dt> <dd>

Ein Deltapatch ist ein deltakomprimiertes Windows Installer-Patch, der mit einem Tool wie Patchwiz.dll erstellt wurde, das die Deltakomprimierung unterstützt. Patches, die die Deltakomprimierung verwenden, können die Größe eines Updates verringern, indem sie nur die Unterschiede (Deltas) zwischen vorhandenen Dateien auf einem Zielcomputer und den gewünschten neuen Dateien bereitstellen. Die gewünschten neuen Dateien werden dann aus den vorhandenen Dateien und den heruntergeladenen Deltas synthetisiert. Weitere Informationen zur Deltakomprimierungstechnologie finden Sie unter [Delta Compression Application Programming Interface](https://msdn.microsoft.com/library/ms811406.aspx).

</dd> </dl>

 

 



