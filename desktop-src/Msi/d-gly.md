---
description: Erfahren Sie mehr über Windows Installer Konzepte, die mit dem Buchstaben D beginnen, z. B. Datenbankfunktion und Deltapatch.
ms.assetid: d6dd73e7-657f-4f71-8e9b-70369cb21972
title: D (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d76378d636c8ae14acdc9cb882c31840e3f1550f
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010933"
---
# <a name="d-windows-installer"></a>D (Windows Installer)

[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) D [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z

<dl> <dt>

<span id="_msi_database_function_gly"></span><span id="_MSI_DATABASE_FUNCTION_GLY"></span>**Datenbankfunktion**
</dt> <dd>

Greift auf die Installationsdatenbank zu. Diese Funktionen werden in erster Linie für die Verwendung durch [*Installer-Paketerstellungstools*](i-gly.md) bereitgestellt und sind nicht für den Aufruf von Installationsprogrammdiensten vorgesehen. Weitere Informationen finden Sie unter [Datenbankfunktionen](database-functions.md) und die [Installer-Funktionsreferenz.](installer-function-reference.md)

</dd> <dt>

<span id="_msi_database_handle_gly"></span><span id="_MSI_DATABASE_HANDLE_GLY"></span>**Datenbankhandle**
</dt> <dd>

Erforderlich für die Arbeit mit einer Datenbank. Weitere Informationen finden Sie unter [Abrufen eines Datenbankhandle.](obtaining-a-database-handle.md)

</dd> <dt>

<span id="setup.delta_patch_gly"></span><span id="SETUP.DELTA_PATCH_GLY"></span>**Deltapatch**
</dt> <dd>

Ein Deltapatch ist ein deltakomprimiertes Windows Installer Patch, der mit einem Tool wie Patchwiz.dll erstellt wurde, das die Deltakomprimierung unterstützt. Patches, die die Deltakomprimierung verwenden, können die Größe eines Updates reduzieren, indem nur die Unterschiede (Deltas) zwischen vorhandenen Dateien auf einem Zielcomputer und den gewünschten neuen Dateien zur Verfügung gestellt werden. Die gewünschten neuen Dateien werden dann aus den vorhandenen Dateien und den heruntergeladenen Deltas synthetisiert. Weitere Informationen zur Deltakomprimierungstechnologie finden Sie unter Anwendungsprogrammierschnittstelle für die [Deltakomprimierung.](https://msdn.microsoft.com/library/ms811406.aspx)

</dd> </dl>

 

 



