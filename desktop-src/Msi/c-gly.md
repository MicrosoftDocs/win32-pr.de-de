---
description: Erfahren Sie Windows Installer-Konzepte, die mit dem Buchstaben C beginnen, z. B. die Schränkdatei und die Prüfsumme.
ms.assetid: f98d19c5-5187-4718-b241-3ec69454c2d6
title: C (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fb0e9a1f14a3b2a7f47722d8db3e3d9cb8356df500e54dbf581bd919afb5765
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119581780"
---
# <a name="c-windows-installer"></a>C (Windows Installer)

[A](a-gly.md) [B](b-gly.md) C [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) T [](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z

<dl> <dt>

<span id="_msi_cabinet_file_using_windows_installer_gly"></span><span id="_MSI_CABINET_FILE_USING_WINDOWS_INSTALLER_GLY"></span>**Datei "cabinet"**
</dt> <dd>

Einzelne Datei, in der Regel mit .cab Erweiterung, die komprimierte Dateien in einer Dateibibliothek speichert. Das Schränkformat ist eine effiziente Möglichkeit, mehrere Dateien zu verpacken, da die Komprimierung über Dateigrenzen hinweg durchgeführt wird, was das Komprimierungsverhältnis erheblich verbessert. Informationen zum Erstellen von Schränken finden Sie unter [Cabinet Files](cabinet-files.md).

</dd> <dt>

<span id="_msi_checksum_gly"></span><span id="_MSI_CHECKSUM_GLY"></span>**Prüfsumme**
</dt> <dd>

Berechneter Wert, der vom Inhalt einer Datei abhängt. Es wird mit Daten gespeichert, um Dateibeschädigungen zu erkennen. Das System überprüft diesen Wert, um sicherzustellen, dass die Daten nicht korrupiert sind.

</dd> <dt>

<span id="_msi_component_using_windows_installer_gly"></span><span id="_MSI_COMPONENT_USING_WINDOWS_INSTALLER_GLY"></span>**Komponente**
</dt> <dd>

Der kleinste Teil einer Installation, der vom Installationsprogramm verarbeitet wird, auch ein Baustein einer Anwendung oder eines Features aus Sicht des Programmierers. Beispiele für Komponenten sind eine Gruppe verwandter Dateien, ein COM-Objekt oder eine Bibliothek. Weitere Informationen finden Sie unter [Komponenten und Funktionen](components-and-features.md).

</dd> <dt>

<span id="_msi_committing_databases_using_windows_installer_gly"></span><span id="_MSI_COMMITTING_DATABASES_USING_WINDOWS_INSTALLER_GLY"></span>**Committen von Datenbanken**
</dt> <dd>

Akkumulierte Änderungen, die in einer Datenbank vorgenommen wurden. Die Änderungen werden erst in der tatsächlichen Datenbank widergespiegelt, wenn ein Committed für die Datenbank vorgenommen wurde. Weitere Informationen finden Sie unter [Committen von Datenbanken.](committing-databases.md)

</dd> <dt>

<span id="_msi_controlevent_gly"></span><span id="_MSI_CONTROLEVENT_GLY"></span>**ControlEvent**
</dt> <dd>

Aspekt der Funktionalität der Benutzeroberfläche des Installationsprogramms. Ein typisches ControlEvent löst eine Aktion durch das Installationsprogramm aus, wenn ein Dialogfeld-Steuerelement oder ein anderes Ereignis aktiviert wird. Weitere Informationen finden Sie unter [ControlEvent Overview (Übersicht über ControlEvent).](controlevent-overview.md)

</dd> <dt>

<span id="_msi_costing_gly"></span><span id="_MSI_COSTING_GLY"></span>**Kostet**
</dt> <dd>

Methode, die vom Installationsprogramm verwendet wird, um die Speicherplatzanforderungen für die Installation zu bestimmen. Bei der Kostenkalkulation werden Faktoren berücksichtigt, z. B. ob vorhandene Dateien überschrieben werden müssen. Weitere Informationen finden Sie unter [Dateikosten.](file-costing.md)

</dd> <dt>

<span id="_msi_.cub_file_gly"></span><span id="_MSI_.CUB_FILE_GLY"></span>**CUB-Datei**
</dt> <dd>

Validierungsmodul, das benutzerdefinierte ICE-Aktionen speichert und zugriff. Weitere Informationen finden Sie unter [CUB-Beispieldatei.](sample--cub-file.md) Weitere Informationen finden Sie auch unter Windows [Installer File Extensions](windows-installer-file-extensions.md).

</dd> <dt>

<span id="_msi_custom_action_using_windows_installer_gly"></span><span id="_MSI_CUSTOM_ACTION_USING_WINDOWS_INSTALLER_GLY"></span>**Benutzerdefinierte Aktion**
</dt> <dd>

Wurde vom Autor des Pakets [*geschrieben,*](p-gly.md) aber nicht als Standardaktion in das Installationsprogramm integriert. Weitere Informationen finden Sie unter [Benutzerdefinierte Aktionen.](custom-actions.md)

</dd> </dl>

 

 



