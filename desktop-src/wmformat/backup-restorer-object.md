---
title: Backup Restorer-Objekt
description: Backup Restorer-Objekt
ms.assetid: 83ce28c0-fd17-46ff-94c0-d28124a0e56a
keywords:
- Windows Media-Format-SDK, Backup Restorer Objects
- Advanced Systems Format (ASF), Backup Restorer Objects
- ASF (Advanced Systems Format), Backup Restorer Objects
- Objekte, Backup Restorer Objects
- Backup Restorer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d08e8bec9bb7bbc2a45fbf632e69d230a2536633
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "106338043"
---
# <a name="backup-restorer-object"></a>Backup Restorer-Objekt

Der Backup Restorer bietet Schnittstellen zum Sichern von Lizenzen, in der Regel auf Wechselmedien und zum anschließenden Wiederherstellen dieser Lizenzen auf einem neuen Computer.

Das Backup Restorer-Objekt wird von der [**wmkreatebackuprestorer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatebackuprestorer) -Funktion erstellt, mit der ein Zeiger auf eine [**iwmlicensebackup**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup) -Schnittstelle festgelegt wird. Die anderen Schnittstellen des Backup Restorer-Objekts können durch Aufrufen der **QueryInterface** -Methode abgerufen werden.

Die folgenden Schnittstellen werden vom Backup Restorer-Objekt unterstützt.



| Schnittstelle                                              | BESCHREIBUNG                                                                                                                                               |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Iwmbackuprestore-Eigenschaften**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbackuprestoreprops) | Legt die Eigenschaften fest, die von den Schnittstellen [**iwmlicensebackup**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup) und [**iwmlicenserestore**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserestore) benötigt werden, oder ruft Sie ab. |
| [**Iwmlicenlbackup**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup)           | Sichert Lizenzen, in der Regel, damit Sie auf einem anderen Computer wieder hergestellt werden können.                                                                          |
| [**Iwmlicenserestore**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserestore)         | Stellt Lizenzen wieder her.                                                                                                                                        |



 

Die folgende Rückruf Schnittstelle muss von der Anwendung implementiert werden, damit das Backup Restorer-Objekt verwendet werden soll.



| Schnittstelle                                      | BESCHREIBUNG                                                                |
|------------------------------------------------|----------------------------------------------------------------------------|
| [**Iwmstatus Callback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | Empfängt Statusmeldungen von Prozessen, die in einem separaten Thread ausgeführt werden. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Sichern und Wiederherstellen von Lizenzen**](backing-up-and-restoring-licenses.md)
</dt> <dt>

[**Objekte**](objects.md)
</dt> </dl>

 

 




