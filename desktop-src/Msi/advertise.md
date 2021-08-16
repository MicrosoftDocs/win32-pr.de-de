---
description: Der Wert der ADVERTISE-Eigenschaft ist eine Liste von Features, die durch Kommas getrennt sind, die angekündigt werden sollen.
ms.assetid: ef97f70b-e4bf-4eb3-b643-046a9c348823
title: ADVERTISE-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da43d291b64ed10c1ae5321a766eca6cab9c4423a26625aacd92e9591d2e3f6d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118381599"
---
# <a name="advertise-property"></a>ADVERTISE-Eigenschaft

Der Wert der **ADVERTISE-Eigenschaft** ist eine Liste von Features, die durch Kommas getrennt sind, die angekündigt werden sollen. Die Features müssen in der Spalte Feature der Tabelle [Feature vorhanden](feature-table.md) sein. Um alle Features wie angekündigt zu installieren, verwenden Sie ADVERTISE=ALL in der Befehlszeile. Geben Sie ADVERTISE=ALL nicht in die [Tabelle Eigenschaft ein,](property-table.md) da dadurch ein angekündigtes Paket generiert wird, das nicht installiert oder entfernt werden kann.

## <a name="remarks"></a>Hinweise

Beachten Sie, dass bei Featurenamen die Schreibung beachtet wird.

Das Installationsprogramm wertet die folgenden Eigenschaften immer in der folgenden Reihenfolge aus.

1.  [**ADDLOCAL**](addlocal.md)
2.  [**Entfernen**](remove.md)
3.  [**ADDSOURCE**](addsource.md)
4.  [**ADDDEFAULT**](adddefault.md)
5.  [**Installieren**](reinstall.md)
6.  **Werben**
7.  [**COMPADDLOCAL**](compaddlocal.md)
8.  [**COMPADDSOURCE**](compaddsource.md)
9.  [**COMPADDDEFAULT**](compadddefault.md)
10. [**FILEADDLOCAL**](fileaddlocal.md)
11. [**FILEADDSOURCE**](fileaddsource.md)
12. [**FILEADDDEFAULT**](fileadddefault.md)

Wenn die Befehlszeile z. B. FOLGENDEs angibt: ADDLOCAL=ALL, ADDSOURCE = MyFeature, werden alle Features zuerst auf run-local und dann myFeature auf run-from-source festgelegt. Wenn die Befehlszeile auf ADDSOURCE=ALL, ADDLOCAL=MyFeature festgelegt ist, wird zuerst MyFeature auf run-local festgelegt, und wenn ADDSOURCE=ALL ausgewertet wird, werden alle Features (einschließlich MyFeature) auf die Ausführung aus der Quelle zurückgesetzt.

Das Installationsprogramm legt die [**Preselected-Eigenschaft**](preselected.md) während der Wiederaufnahme einer angehaltenen Installation oder bei Angabe einer der oben genannten Eigenschaften in der Befehlszeile auf den Wert "1" fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP. Informationen zum [Windows Service](windows-installer-portal.md) Pack, das für eine Windows Installer-Version erforderlich ist, finden Sie unter Windows Installer Run-Time Anforderungen.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> </dl>

 

 




