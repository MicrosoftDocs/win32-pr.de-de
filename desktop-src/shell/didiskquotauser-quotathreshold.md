---
description: Legt den Warnungs Schwellenwert des Benutzers in Bytes fest oder ruft ihn ab.
ms.assetid: 5289d472-d591-4604-91f9-252dd4a1b62b
title: Didiskquotauser. quotathreshold (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.QuotaThreshold
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 7ce336c84d086c4e4be369278a77e40e59474bc5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862115"
---
# <a name="didiskquotauserquotathreshold-property"></a>Didiskquotauser. quotathreshold (Eigenschaft)

Legt den Warnungs Schwellenwert des Benutzers in Bytes fest oder ruft ihn ab.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```JScript
iQuotaThreshold = DIDiskQuotaUser.QuotaThreshold
DIDiskQuotaUser.QuotaThreshold = iQuotaThreshold
```



## <a name="property-value"></a>Eigenschaftswert

Ein **ganzzahliger** Wert, der den Warnungs Schwellenwert des Benutzers angibt oder empfängt. Wenn die Datenträger Nutzung eines Benutzers diesen Wert überschreitet und die [**logquotathreshold**](diskquotacontrol-logquotathreshold.md) -Eigenschaft auf **true** festgelegt ist, generiert das System einen Ereignisprotokoll Eintrag.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5,0 oder höher)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Defaultquotathreshold**](diskquotacontrol-defaultquotathreshold.md)
</dt> <dt>

[**Didiskquotauser**](didiskquotauser-object.md)
</dt> <dt>

[**QuotaLimit**](didiskquotauser-quotalimit.md)
</dt> <dt>

[**Quotader OLDTEXT**](didiskquotauser-quotathresholdtext.md)
</dt> </dl>

 

 




