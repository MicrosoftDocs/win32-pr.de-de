---
description: Die ADMIN-Aktion ist eine Aktion der obersten Ebene, die zum Ausführen von Administratorinstallationen verwendet wird.
ms.assetid: 9925a645-5909-42c7-9de8-f908a5e42be9
title: ADMIN-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 785bd69a8de7da1df9a812f7e89d589b6e939b3eedd6b3cecb66bf86407636cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145933"
---
# <a name="admin-action"></a>ADMIN-Aktion

Die ADMIN-Aktion ist eine Aktion der obersten Ebene, die zum Ausführen [von Administratorinstallationen](administrative-installation.md)verwendet wird.

## <a name="sequence-restrictions"></a>Sequenzeinschränkungen

Es gibt keine Sequenzeinschränkungen.

## <a name="actiondata-messages"></a>ActionData-Nachrichten

Es sind keine ActionData-Meldungen vorhanden.

## <a name="remarks"></a>Hinweise

Die ADMIN-Aktion wird nicht innerhalb der Aktionstabellensequenz aufgerufen, Windows Installer diese Aktion ausführt, wenn [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) aufgerufen wird, wobei der *szCommandLine-Parameter* auf "ACTION=ADMIN" festgelegt ist oder die ausführbare Befehlszeilendatei Msiexec.exe mit dem Befehlszeilenschalter "/a" aufgerufen wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[AdminUISequence-Tabelle](adminuisequence-table.md)
</dt> <dt>

[AdminExecuteSequence-Tabelle](adminexecutesequence-table.md)
</dt> </dl>

 

 



