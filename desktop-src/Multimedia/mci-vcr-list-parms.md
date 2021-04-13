---
title: MCI_VCR_LIST_PARMS Struktur (VCR. h)
description: Die Struktur der MCI- \_ VCR- \_ Listen \_ Parameter enthält Parameter für den MCI- \_ Listen Befehl für Video-Kassetten-Recorder.
ms.assetid: 88725599-8057-4787-96e6-49b4a651c894
keywords:
- MCI_VCR_LIST_PARMS Struktur Windows Multimedia
topic_type:
- apiref
api_name:
- MCI_VCR_LIST_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d3e7a2eae67ebc7148b7ff424361f16554a435c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341157"
---
# <a name="mci_vcr_list_parms-structure"></a>Struktur von MCI- \_ VCR- \_ Listen- \_ Parametern

Die Struktur der **MCI- \_ VCR- \_ Listen \_** Parameter enthält Parameter für den [**MCI- \_ Listen**](mci-list.md) Befehl für Video-Kassetten-Recorder.

## <a name="syntax"></a>Syntax


```C++
typedef struct tagMCI_VCR_LIST_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwReturn;
  DWORD     dwNumber;
} MCI_VCR_LIST_PARMS;
```



## <a name="members"></a>Member

<dl> <dt>

**dwcallback**
</dt> <dd>

Das nieder wertige Wort gibt ein Fenster Handle an, das für das MCI-Benachrichtigungs Kennzeichen verwendet wird \_ .

</dd> <dt>

**dwreturn**
</dt> <dd>

Der Puffer für die zurückgegebenen Informationen.

</dd> <dt>

**dwnumber**
</dt> <dd>

Die Anzahl der Video-oder Audioeingaben von VCR.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn Sie den Membern dieser Strukturdaten zuweisen, legen Sie die entsprechenden Flags im *fdwcommand* -Parameter der [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion fest, um die Elemente zu überprüfen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                       |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                             |
| Header<br/>                   | <dl> <dt>VCR. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MCI**](mci.md)
</dt> <dt>

[**MCI-Strukturen**](mci-structures.md)
</dt> <dt>

[**MCI- \_ Liste**](mci-list.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

