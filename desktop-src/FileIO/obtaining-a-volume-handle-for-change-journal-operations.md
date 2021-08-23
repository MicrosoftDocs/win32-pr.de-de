---
description: 'Um ein Handle für ein Volume für die Verwendung mit Änderungsjournalvorgängen der Updatesequenznummer (USN) abzurufen, rufen Sie die CreateFile-Funktion auf, wobei der lpFileName-Parameter auf eine Zeichenfolge in der folgenden Form festgelegt ist: \\ \\ . \\ X.'
ms.assetid: a4f4dac5-76fd-4e9e-a71e-665684840d74
title: Abrufen eines Volumehandle für Change Journal-Vorgänge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3a7e8090e419df2034d1e1e1726dd74cf2b2915f6976a042a47c73544fa6b38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119683480"
---
# <a name="obtaining-a-volume-handle-for-change-journal-operations"></a>Abrufen eines Volumehandle für Change Journal-Vorgänge

Um ein Handle für ein Volume für die Verwendung mit Änderungsjournalvorgängen der Updatesequenznummer (USN) abzurufen, rufen Sie die [**CreateFile-Funktion**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) auf, wobei der *lpFileName-Parameter* auf eine Zeichenfolge in der folgenden Form festgelegt ist: \\ \\ . \\ *X*:

Beachten Sie, dass *X* der Buchstabe ist, der das Laufwerk identifiziert, auf dem das NTFS-Volume angezeigt wird.

Wenn das Volume keinen Laufwerkbuchstaben aufweist, verwenden Sie die unter [Benennen eines Volumes](naming-a-volume.md)beschriebene Syntax.

 

 



