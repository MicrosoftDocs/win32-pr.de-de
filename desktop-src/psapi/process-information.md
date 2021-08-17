---
title: Prozessinformationen
description: Das System verwaltet eine Liste der ausgeführten Prozesse. Sie können die Bezeichner für diese Prozesse abrufen, indem Sie die EnumProcesses-Funktion aufrufen. Diese Funktion füllt ein Array von DWORD-Werten mit den Bezeichnern aller Prozesse im System auf.
ms.assetid: 229c661e-9c33-47a3-9441-558cfe2a800d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5facb72f094059997c271cb9f38beaea08981430bba40902d620a23e2875b26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119094891"
---
# <a name="process-information"></a>Prozessinformationen

Das System verwaltet eine Liste der ausgeführten Prozesse. Sie können die Bezeichner für diese Prozesse abrufen, indem Sie die [**EnumProcesses-Funktion**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses) aufrufen. Diese Funktion füllt ein Array von **DWORD-Werten** mit den Bezeichnern aller Prozesse im System auf.

Viele Funktionen in PSAPI erfordern ein Prozesshand handle. Um ein Prozesshand handle für einen ausgeführten Prozess zu erhalten, übergeben Sie seinen Prozessbezeichner (aus [**EnumProcesses**](/windows/desktop/api/Psapi/nf-psapi-enumprocesses)) an die [**OpenProcess-Funktion.**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess) Denken Sie daran, die [**CloseHandle-Funktion auf**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) aufruft, wenn Sie mit dem Prozesshandle fertig sind.

 

 