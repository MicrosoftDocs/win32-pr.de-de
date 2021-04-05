---
description: Die Aktion ankündigen ist eine Aktion der obersten Ebene, die zum Installieren oder Entfernen von angekündigten Komponenten aufgerufen wird.
ms.assetid: d9c843e4-fcd9-4d47-9ca9-ffa83ed80574
title: Aktion ankündigen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0985990d69863f250cfd6f589deb43a59f9c66e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756246"
---
# <a name="advertise-action"></a>Aktion ankündigen

Die Aktion ankündigen ist eine Aktion der obersten Ebene, die zum Installieren oder Entfernen von angekündigten Komponenten aufgerufen wird.

## <a name="sequence-restrictions"></a>Sequenz Einschränkungen

Es gibt keine Sequenz Einschränkungen.

## <a name="actiondata-messages"></a>Aktions Daten Meldungen

Es sind keine Aktions Daten Meldungen vorhanden.

## <a name="remarks"></a>Bemerkungen

[*Werbung*](a-gly.md) bezieht sich auf die Fähigkeit des Installers, die Lade-und Start Schnittstellen einer Anwendung bereitzustellen, ohne die Anwendung physisch zu installieren. Der Installer installiert die erforderlichen Komponenten erst, wenn ein Benutzer oder eine Anwendung eine angekündigte Benutzeroberfläche aktiviert. Dieses Konzept wird als [*install-on-Demand*](i-gly.md)bezeichnet.

Die Ankündigungs Aktion wird nicht innerhalb der Aktions Tabellen Sequenz aufgerufen. die Windows Installer führt diese Aktion aus, wenn die ausführbare Befehlszeilen Datei Msiexec.exe mit dem Befehls Zeilenschalter '/j ' aufgerufen wird oder wenn ' [**msiinstallproduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) ' aufgerufen wird, wobei der *szcommandline* -Parameter auf Action = Ankündigungs Wert festgelegt ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[AdvtExecuteSequence-Tabelle](advtexecutesequence-table.md)
</dt> </dl>

 

 



