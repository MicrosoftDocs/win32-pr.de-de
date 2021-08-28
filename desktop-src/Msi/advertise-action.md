---
description: Die AKTION "ADVERTISE" ist eine Aktion der obersten Ebene, die aufgerufen wird, um angekündigte Komponenten zu installieren oder zu entfernen.
ms.assetid: d9c843e4-fcd9-4d47-9ca9-ffa83ed80574
title: ADVERTISE-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd70b36edfb0074911ee3c9487a299f3c0b2eb4bacc59f05241fc6ee22119800
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045930"
---
# <a name="advertise-action"></a>ADVERTISE-Aktion

Die AKTION "ADVERTISE" ist eine Aktion der obersten Ebene, die aufgerufen wird, um angekündigte Komponenten zu installieren oder zu entfernen.

## <a name="sequence-restrictions"></a>Sequenzeinschränkungen

Es gibt keine Sequenzeinschränkungen.

## <a name="actiondata-messages"></a>ActionData-Nachrichten

Es sind keine ActionData-Meldungen vorhanden.

## <a name="remarks"></a>Hinweise

[*Werbung*](a-gly.md) bezieht sich auf die Fähigkeit des Installationsprogramms, die Lade- und Startschnittstellen einer Anwendung bereitzustellen, ohne die Anwendung physisch zu installieren. Das Installationsprogramm installiert die erforderlichen Komponenten erst, wenn ein Benutzer oder eine Anwendung eine angekündigte Schnittstelle aktiviert. Dieses Konzept wird als [*install-on-demand*](i-gly.md)bezeichnet.

Die AKTION ADVERTISE wird nicht innerhalb der Aktionstabellensequenz aufgerufen. Der Windows Installer führt diese Aktion aus, wenn die ausführbare Befehlszeilendatei Msiexec.exe mit dem Befehlszeilenschalter "/j" aufgerufen wird oder [**wenn MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) aufgerufen wird, wobei der *szCommandLine-Parameter* auf ACTION=ADVERTISE festgelegt ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Tabelle "AdvtExecuteSequence"](advtexecutesequence-table.md)
</dt> </dl>

 

 



