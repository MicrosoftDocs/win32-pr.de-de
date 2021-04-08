---
title: LVN_GETDISPINFO Benachrichtigungs Code (kommctrl. h)
description: Wird von einem Listenansicht-Steuerelement an das übergeordnete Fenster gesendet. Es ist eine Anforderung für das übergeordnete Fenster, Informationen bereitzustellen, die zum Anzeigen oder Sortieren eines Listen Ansichts Elements erforderlich sind. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 04310e39-69bc-45d7-958c-00452279d7a9
keywords:
- Windows-Steuerelemente für LVN_GETDISPINFO Benachrichtigungs
topic_type:
- apiref
api_name:
- LVN_GETDISPINFO
- LVN_GETDISPINFOA
- LVN_GETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1585524dd447c4a1324dc5c7a235490de776fb2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103744001"
---
# <a name="lvn_getdispinfo-notification-code"></a>LVN \_ getdispinfo-Benachrichtigungs Code

Wird von einem Listenansicht-Steuerelement an das übergeordnete Fenster gesendet. Es ist eine Anforderung für das übergeordnete Fenster, Informationen bereitzustellen, die zum Anzeigen oder Sortieren eines Listen Ansichts Elements erforderlich sind. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.


```C++
LVN_GETDISPINFO
        
    pdi = (NMLVDISPINFO*) lParam
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**nmlvdispinfo**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) -Struktur. Bei der Eingabe gibt die in dieser Struktur enthaltene [**lvitem**](/windows/win32/api/commctrl/ns-commctrl-lvitema) -Struktur den Typ der erforderlichen Informationen an und identifiziert das Element oder Unterelement, das von Interesse ist. Verwenden Sie die **lvitem** -Struktur, um die angeforderten Informationen an das-Steuerelement zurückzugeben. Wenn Ihr Meldungs Handler das lvif \_ di \_ SetItem-Flag im **Masken** -Member der **lvitem** -Struktur festlegt, speichert das Listenansicht-Steuerelement die angeforderten Informationen und fragt es nicht erneut ab.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

Der Benachrichtigungs Empfänger wandelt *LPARAM* ein, um die [**nmlvdispinfo**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) -Struktur abzurufen. Der *wParam* -Parameter enthält den Benachrichtigungs Code.

Ein Listenansicht-Steuerelement sendet den **LVN \_ getdispinfo** -Benachrichtigungs Code zum Abrufen von Element Informationen, die von der Anwendung gespeichert werden, und nicht vom-Steuerelement. Die Informationen können Text-oder Symbol Informationen für ein Element sein. Dabei kann es sich auch um Element Zustandsinformationen handeln. Weitere Informationen zum Implementieren des Element Zustands auf Rückruf Basis finden Sie in der [**LVM- \_ SetCallbackMask**](lvm-setcallbackmask.md) -Nachricht.

Weitere Informationen zu List-View-Rückrufen finden Sie unter [Rückruf Elemente und Rückruf Maske](list-view-controls-overview.md).

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt, wie dieser Benachrichtigungs Code behandelt werden kann, um den Text in den Spalten einer Listenansicht festzulegen. Die Daten für jedes Element werden in der folgenden Struktur gespeichert.


```C++
 typedef struct tagPETINFO
{
    TCHAR szName[50];
    TCHAR szBreed[50];
    TCHAR szGender[7];
    TCHAR szPrice[20];
    GroupIds iGroup;
} PETINFO;
            
```



Der WM- \_ Benachrichtigungs Handler in der Dialogfeld Prozedur lautet wie folgt:


```C++
    case WM_NOTIFY:
        switch (((LPNMHDR) lParam)->code)
        {
        case LVN_GETDISPINFO:
            {
                NMLVDISPINFO* plvdi = (NMLVDISPINFO*)lParam;    
                switch (plvdi->item.iSubItem)
                {
                case 0:
                    // rgPetInfo is an array of PETINFO structures.
                    plvdi->item.pszText = rgPetInfo[plvdi->item.iItem].szName;
                    break;

                case 1:
                    plvdi->item.pszText = rgPetInfo[plvdi->item.iItem].szBreed;
                    break;

                case 2:
                    plvdi->item.pszText = rgPetInfo[plvdi->item.iItem].szGender;
                    break;

                case 3:
                    plvdi->item.pszText = rgPetInfo[plvdi->item.iItem].szPrice;
                    break;

                default:
                    break;
                }
                return TRUE;
            }
      // More notifications...
      }
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Kommstrg. h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **LVN \_ Getdispinfow** (Unicode) und **LVN \_ getdispinfoa** (ANSI)<br/>           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**LVN \_ setdispinfo**](lvn-setdispinfo.md)
</dt> </dl>

 

 





