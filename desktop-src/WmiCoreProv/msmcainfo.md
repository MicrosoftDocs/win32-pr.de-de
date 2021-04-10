---
description: Eine abstrakte Basisklasse, von der alle Daten Klassen des MCA-Anbieters (Machine Check Architecture), wie z. b. msmcainfo \_ rawmcadata, abgeleitet werden. Diese Klasse ist nur in 64-Bit-Windows-Systemen verfügbar.
ms.assetid: 22ec8343-fc4f-4b14-9354-26b5d6a6fe09
title: Msmcainfo-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAInfo
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 31fc35b1d680d900af929ea8a828bcb23d222f66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041718"
---
# <a name="msmcainfo-class"></a>Msmcainfo-Klasse

Bei der **msmcainfo** -Klasse handelt es sich um eine abstrakte Basisklasse, von der alle Daten Klassen des MCA-Anbieters (Machine Check Architecture), wie z. b. [**msmcainfo \_ rawmcadata**](msmcainfo-rawmcadata.md), abgeleitet werden. Der MCA-Anbieter verfügt auch über Ereignis Klassen, die von [**wmievent**](wmievent.md)abgeleitet werden. Diese Klasse ist nur in 64-Bit-Windows-Systemen verfügbar.

Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.

## <a name="syntax"></a>Syntax

``` syntax
class MSMCAInfo
{
};
```

## <a name="members"></a>Member

Die **msmcainfo** -Klasse definiert keine Member.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows XP<br/>                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003<br/>                                                         |
| Namespace<br/>                | WMI-Stammdatei \\<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WMI Core. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wmiprov.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[MSMCA-Klassen](msmca-classes.md)
</dt> <dt>

[**Msmcaevent- \_ Header**](msmcaevent-header.md)
</dt> <dt>

[**WMIEvent**](wmievent.md)
</dt> </dl>

 

 




