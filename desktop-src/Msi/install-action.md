---
description: Die Installations Aktion ist eine Aktion der obersten Ebene, die zum Installieren oder Entfernen von Komponenten aufgerufen wird.
ms.assetid: bf290b59-1ecb-410f-b1f6-fdbeebebe3d3
title: Installations Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04279ba66f189ff83146fc2010e6843c20b404d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042096"
---
# <a name="install-action"></a>Installations Aktion

Die Installations Aktion ist eine Aktion der obersten Ebene, die zum Installieren oder Entfernen von Komponenten aufgerufen wird. Mit dieser Aktion werden die Tabelle " [InstallUISequence](installuisequence-table.md) " und die [Tabelle "InstallExecuteSequence](installexecutesequence-table.md) " für die auszuführende Aktion, die Bedingung für die Ausführung der Aktion und die Position der Aktion in der Sequenz abgefragt:

## <a name="sequence-restrictions"></a>Sequenz Einschränkungen

Es gibt keine Sequenz Einschränkungen.

## <a name="actiondata-messages"></a>Aktions Daten Meldungen

Es sind keine Aktions Daten Meldungen vorhanden.

## <a name="remarks"></a>Bemerkungen

Die Installations Aktion wird nicht innerhalb der Aktions Tabellen Sequenz aufgerufen, Sie wird an Windows Installer weitergegeben, wenn [**msiinstallproduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) aufgerufen wird, oder die ausführbare Befehlszeilen Datei Msiexec.exe mit dem Befehls Zeilenschalter '**/i**' aufgerufen wird, oder wenn eine beliebige Installer-Funktion aufgerufen wird, die möglicherweise eine Installationsaufgabe ausführt, z. b. [**msikonfigurirefeature**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea), [**MsiProvideComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta)oder [**msiinstallmissingfile**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea).

 

 



