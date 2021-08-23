---
title: Sicherungswiederherstellungsobjekt
description: Sicherungswiederherstellungsobjekt
ms.assetid: 83ce28c0-fd17-46ff-94c0-d28124a0e56a
keywords:
- Windows Medienformat-SDK, Sicherungswiederherstellungsobjekte
- Advanced Systems Format (ASF), Sicherungswiederherstellungsobjekte
- ASF (Advanced Systems Format), Sicherungswiederherstellungsobjekte
- Objekte,Sicherungswiederherstellungsobjekte
- Sicherungswiederherstellung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a7bf14f8afda284d8d0ae3d4f36d37fff0baa63f4f42802a98830038ec2d850
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028128"
---
# <a name="backup-restorer-object"></a>Sicherungswiederherstellungsobjekt

Die Sicherungswiederherstellung stellt Schnittstellen bereit, um das Sichern von Lizenzen (in der Regel auf Wechselmedien) und das anschließende Wiederherstellen dieser Lizenzen auf einem neuen Computer zu verarbeiten.

Das Sicherungswiederherstellungsobjekt wird von der [**WMCreateBackupRestorer-Funktion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatebackuprestorer) erstellt, die einen Zeiger auf eine [**IWMLicenseBackup-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup) legt. Die anderen Schnittstellen des Sicherungswiederherstellungsobjekts können durch Aufrufen der **QueryInterface-Methode ermittelt** werden.

Die folgenden Schnittstellen werden vom Sicherungswiederherstellungsobjekt unterstützt.



| Schnittstelle                                              | BESCHREIBUNG                                                                                                                                               |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMBackupRestoreProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbackuprestoreprops) | Legt eigenschaften fest, die für die [**SCHNITTSTELLEN IWMLicenseBackup**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup) und [**IWMLicenseRestore erforderlich**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserestore) sind, und ruft sie ab. |
| [**IWMLicenseBackup**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup)           | Sichern von Lizenzen, in der Regel so, dass sie auf einem anderen Computer wiederhergestellt werden können.                                                                          |
| [**IWMLicenseRestore**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserestore)         | Stellt Lizenzen wieder zur Verfügung.                                                                                                                                        |



 

Die folgende Rückrufschnittstelle muss von der Anwendung implementiert werden, um das Sicherungswiederherstellungsobjekt verwenden zu können.



| Schnittstelle                                      | BESCHREIBUNG                                                                |
|------------------------------------------------|----------------------------------------------------------------------------|
| [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | Empfängt Statusmeldungen von Prozessen, die in einem separaten Thread ausgeführt werden. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Sichern und Wiederherstellen von Lizenzen**](backing-up-and-restoring-licenses.md)
</dt> <dt>

[**Objekte**](objects.md)
</dt> </dl>

 

 




