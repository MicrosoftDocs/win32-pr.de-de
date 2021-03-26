---
title: Prozessinformationen
description: Das System verwaltet eine Liste der laufenden Prozesse. Sie können die Bezeichner für diese Prozesse abrufen, indem Sie die EnumProcesses-Funktion aufrufen. Diese Funktion füllt ein Array von DWORD-Werten mit den bezeichgern aller Prozesse im System.
ms.assetid: 229c661e-9c33-47a3-9441-558cfe2a800d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 147debe36dd2647cd46d19a62b0374f47b73bc58
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315554"
---
# <a name="process-information"></a>Prozessinformationen

Das System verwaltet eine Liste der laufenden Prozesse. Sie können die Bezeichner für diese Prozesse abrufen, indem Sie die [**EnumProcesses**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses) -Funktion aufrufen. Diese Funktion füllt ein Array von **DWORD** -Werten mit den bezeichgern aller Prozesse im System.

Viele Funktionen in PSAPI erfordern ein Prozess handle. Wenn Sie ein Prozess Handle für einen laufenden Prozess abrufen möchten, übergeben Sie die Prozess-ID (abgerufen von [**enumprozessen**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses)) an die [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) -Funktion. Denken Sie daran, die [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) -Funktion aufzurufen, wenn Sie mit dem Prozess handle fertig sind.

 

 