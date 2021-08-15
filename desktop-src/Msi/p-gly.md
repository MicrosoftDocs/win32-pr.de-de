---
description: Erfahren Sie mehr über Windows Installerkonzepte, die mit dem Buchstaben P beginnen, z. B. Paketcode und Patchen.
ms.assetid: 868f5ed3-b179-404b-9462-1d3a179103f8
title: P (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74af2780852bcb59124390042bfdbbc7bf2e7618cdb4167f58b15fc04ab1b15b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118942760"
---
# <a name="p-windows-installer"></a>P (Windows Installer)

[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) P [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) W X Y Z

<dl> <dt>

<span id="_msi_package_using_windows_installer_gly"></span><span id="_MSI_PACKAGE_USING_WINDOWS_INSTALLER_GLY"></span>**Paket**
</dt> <dd>

[*.msi Datei*](m-gly.md) und alle [*externen Quelldateien,*](e-gly.md) auf die von dieser Datei verwiesen werden kann. Ein Paket enthält daher alle Informationen, die der Windows Installer benötigt, um die Benutzeroberfläche auszuführen und die Anwendung zu installieren oder zu deinstallieren. Weitere Informationen finden Sie auch unter [*Installationsprogrammdatenbank*](i-gly.md).

</dd> <dt>

<span id="_msi_package_code_gly"></span><span id="_MSI_PACKAGE_CODE_GLY"></span>**Paketcode**
</dt> <dd>

GUID, die ein bestimmtes Paket identifiziert. Ein eindeutiger Paketcode ist erforderlich, da einige Transformationen oder Patchpakete auf mehrere Anwendungen angewendet werden können oder eine Anwendung auf eine andere Anwendung oder Version aktualisieren kann. Weitere Informationen finden Sie unter [Paketcodes.](package-codes.md)

</dd> <dt>

<span id="_msi_patching_gly"></span><span id="_MSI_PATCHING_GLY"></span>**Patchen**
</dt> <dd>

Methode zum Aktualisieren einer Datei, die nur die geänderten Bits anstelle der gesamten Datei ersetzt. Dies bedeutet, dass Benutzer einen Upgradepatch für ein Produkt herunterladen können, das viel kleiner als das gesamte Produkt ist. Weitere Informationen finden Sie unter [Patchpakete.](patch-packages.md)

</dd> <dt>

<span id="_msi_patch_file_gly"></span><span id="_MSI_PATCH_FILE_GLY"></span>**Patchdatei**
</dt> <dd>

P [atch-Paket, das](patch-packages.md) zum Patchen verwendet wird. Weitere Informationen finden Sie unter [Patchen und Upgrades.](patching-and-upgrades.md)

</dd> <dt>

<span id="_msi_preview_mode_using_windows_installer_gly"></span><span id="_MSI_PREVIEW_MODE_USING_WINDOWS_INSTALLER_GLY"></span>**Vorschaumodus**
</dt> <dd>

Modus zum Anzeigen des Entwurfs der Benutzeroberfläche. Weitere Informationen finden Sie unter [Vorschau der Benutzeroberfläche](previewing-the-user-interface.md).

</dd> <dt>

<span id="_msi_progress_bar_gly"></span><span id="_MSI_PROGRESS_BAR_GLY"></span>**Statusanzeige**
</dt> <dd>

Steuern Sie, ob das Installationsprogramm während der Skriptausführungszeit angezeigt werden kann, die den Fortschritt der Installation darstellt. Weitere Informationen finden Sie unter [Erstellen eines ProgressBar-Steuerelements.](authoring-a-progressbar-control.md)

</dd> <dt>

<span id="_msi_property_gly"></span><span id="_MSI_PROPERTY_GLY"></span>**Eigenschaft**
</dt> <dd>

Globale Variablen, die während einer Installation verwendet werden. (Siehe [Informationen zu Eigenschaften](about-properties.md).)

Der Begriff "Eigenschaft" bezieht sich auch auf ein Attribut eines Automatisierungsobjekts. (Weitere Informationen finden Sie unter [Automation Interface](automation-interface.md).)

</dd> <dt>

<span id="_msi_publishing_gly"></span><span id="_MSI_PUBLISHING_GLY"></span>**Publishing**
</dt> <dd>

Methode zum [*Anwerben*](a-gly.md) eines Features oder einer Anwendung. Bei der Veröffentlichung wird die Benutzeroberfläche nicht aufgefüllt. Wenn jedoch eine andere Anwendung versucht, eine veröffentlichte Anwendung zu öffnen, sind genügend Informationen vorhanden, damit das Installationsprogramm die veröffentlichte Anwendung zuweisen kann. Weitere Informationen finden Sie unter [*Assigning*](a-gly.md) and [Components and Features](components-and-features.md).

</dd> </dl>

 

 



