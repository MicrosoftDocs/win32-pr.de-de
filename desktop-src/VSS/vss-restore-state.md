---
description: 'Während eines Wiederherstellungs Vorgangs kann der Anforderer die IVssBackupComponents:: abtrestorestate-Methode verwenden, um den Typ des laufenden Wiederherstellungs Vorgangs zu definieren.'
ms.assetid: f6bf1979-7604-450f-8988-2a17da6b82d7
title: VSS-Wiederherstellungs Status
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97581d33f5695890ba83e87c6f6155a9e7f92f78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368083"
---
# <a name="vss-restore-state"></a>VSS-Wiederherstellungs Status

Während eines Wiederherstellungs Vorgangs kann der Anforderer die [**IVssBackupComponents:: abtrestorestate**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestorestate) -Methode verwenden, um den Typ des laufenden Wiederherstellungs Vorgangs zu definieren. Bei den meisten Wiederherstellungs Vorgängen muss der Standard Wiederherstellungstyp (VSS \_ rtype nicht definiert) jedoch nicht überschrieben werden \_ . Writer sollten diesen wiederherungstyp so behandeln, als wäre er VSS \_ rtype \_ by \_ Copy. Weitere Informationen zu den Werten des Wiederherstellungs Typs finden Sie in der Enumeration des [**VSS- \_ Wiederherstellungs \_ Typs**](/windows/desktop/api/Vss/ne-vss-vss_restore_type) .

 

 



