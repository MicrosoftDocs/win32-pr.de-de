---
description: Die INSTALL-Aktion ist eine Aktion der obersten Ebene, die aufgerufen wird, um Komponenten zu installieren oder zu entfernen.
ms.assetid: bf290b59-1ecb-410f-b1f6-fdbeebebe3d3
title: INSTALL-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b5f648084b7386465f6bb59dd6b523cb51489e4cb83677c0b5cb47fe845be42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119811000"
---
# <a name="install-action"></a>INSTALL-Aktion

Die INSTALL-Aktion ist eine Aktion der obersten Ebene, die aufgerufen wird, um Komponenten zu installieren oder zu entfernen. Diese Aktion fragt die [Tabelle InstallUISequence](installuisequence-table.md) und die [InstallExecuteSequence-Tabelle](installexecutesequence-table.md) nach der auszuführenden Aktion, der Bedingung für die Aktionsausführung und der Position der Aktion in der Sequenz ab:

## <a name="sequence-restrictions"></a>Sequenzeinschränkungen

Es gibt keine Sequenzeinschränkungen.

## <a name="actiondata-messages"></a>ActionData-Nachrichten

Es sind keine ActionData-Meldungen vorhanden.

## <a name="remarks"></a>Hinweise

Die INSTALL-Aktion wird nicht innerhalb der Aktionstabellensequenz aufgerufen, sie wird an Windows Installer übergeben, wenn [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) aufgerufen wird, oder die ausführbare Befehlszeilendatei Msiexec.exe mit dem Befehlszeilenschalter **"/i"** aufgerufen wird, oder wenn eine Installationsprogrammfunktion aufgerufen wird, die eine Installationsaufgabe ausführen kann, z. B. [**MsiConfigureFeature,**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea) [**MsiProvideComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta)oder [**MsiInstallMissingFile**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea).

 

 



