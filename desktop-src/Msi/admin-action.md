---
description: Die Administrator Aktion ist eine Aktion der obersten Ebene, mit der administrative Installationen durchgeführt werden.
ms.assetid: 9925a645-5909-42c7-9de8-f908a5e42be9
title: Administrator Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00106c9ab7877918e122f1ec9bd201fe30bb68b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864508"
---
# <a name="admin-action"></a>Administrator Aktion

Die Administrator Aktion ist eine Aktion der obersten Ebene, mit der [administrative Installationen](administrative-installation.md)durchgeführt werden.

## <a name="sequence-restrictions"></a>Sequenz Einschränkungen

Es gibt keine Sequenz Einschränkungen.

## <a name="actiondata-messages"></a>Aktions Daten Meldungen

Es sind keine Aktions Daten Meldungen vorhanden.

## <a name="remarks"></a>Bemerkungen

Die admin-Aktion wird nicht innerhalb der Aktions Tabellen Sequenz aufgerufen, Windows Installer diese Aktion ausführt, wenn [**msiinstallproduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) mit dem Parameter " *szcommandline* " aufgerufen wird, der auf "action = admin" festgelegt ist, oder die ausführbare Befehlszeilen Datei Msiexec.exe mit dem Befehls Zeilenschalter "/a" aufgerufen wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[AdminUISequence-Tabelle](adminuisequence-table.md)
</dt> <dt>

[AdminExecuteSequence-Tabelle](adminexecutesequence-table.md)
</dt> </dl>

 

 



