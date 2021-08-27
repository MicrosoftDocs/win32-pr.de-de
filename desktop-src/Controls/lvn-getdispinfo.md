---
title: LVN_GETDISPINFO Benachrichtigungscode (Commctrl.h)
description: Wird von einem Listenansicht-Steuerelement an das übergeordnete Fenster gesendet. Es ist eine Anforderung an das übergeordnete Fenster, Informationen zum Anzeigen oder Sortieren eines Listenansichtselements zu liefern. Dieser Benachrichtigungscode wird in Form einer WM \_ NOTIFY-Nachricht gesendet.
ms.assetid: 04310e39-69bc-45d7-958c-00452279d7a9
keywords:
- LVN_GETDISPINFO Benachrichtigungscode Windows Steuerelementen
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
ms.openlocfilehash: 1f4f4fc6917b0de699d1ca561f46bc7789aa15eea7c40aa3681fe74991e3a122
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088820"
---
# <a name="lvn_getdispinfo-notification-code"></a>LVN \_ GETDISPINFO-Benachrichtigungscode

Wird von einem Listenansicht-Steuerelement an das übergeordnete Fenster gesendet. Es ist eine Anforderung an das übergeordnete Fenster, Informationen zum Anzeigen oder Sortieren eines Listenansichtselements zu liefern. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet.


```C++
LVN_GETDISPINFO
        
    pdi = (NMLVDISPINFO*) lParam
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*lParam* 
</dt> <dd>

Zeiger auf eine [**NMLVDISPINFO-Struktur.**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) Bei der Eingabe gibt die in dieser Struktur enthaltene [**LVITEM-Struktur**](/windows/win32/api/commctrl/ns-commctrl-lvitema) den Typ der erforderlichen Informationen an und identifiziert das gewünschte Element oder Unterelement. Verwenden Sie die **LVITEM-Struktur,** um die angeforderten Informationen an das Steuerelement zurück zu geben. Wenn ihr Meldungshandler das LVIF DI SETITEM-Flag im Maskenmitglied der \_ \_ **LVITEM-Struktur** festgelegt hat,  speichert das Listenansicht-Steuerelement die angeforderten Informationen und fordert sie nicht erneut an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

Der Benachrichtigungsempfänger casts *lParam,* um die [**NMLVDISPINFO-Struktur**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) abzurufen. Der *wParam-Parameter* enthält den Benachrichtigungscode.

Ein Listenansicht-Steuerelement sendet den **LVN GETDISPINFO-Benachrichtigungscode, \_** um Elementinformationen abzurufen, die von der Anwendung und nicht vom -Steuerelement gespeichert werden. Die Informationen können Text- oder Symbolinformationen für ein Element sein. Es kann sich auch um Elementzustandsinformationen geben. Weitere Informationen zum Implementieren des Elementzustands auf Rückrufbasis finden Sie in der [**LVM \_ SETCALLBACKMASK-Nachricht.**](lvm-setcallbackmask.md)

Weitere Informationen zu Rückrufen in Listenansichten finden Sie unter [Rückrufelemente und die Rückrufmaske.](list-view-controls-overview.md)

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt, wie dieser Benachrichtigungscode behandelt werden kann, um den Text in den Spalten einer Listenansicht zu setzen. Die Daten für jedes Element werden in der folgenden Struktur gespeichert.


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



Folgendes wird vom WM \_ NOTIFY-Handler in der Dialogprozedur verwendet.


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
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                        |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Unicode- und ANSI-Name<br/>   | **LVN \_ GETDISPINFOW** (Unicode) und **LVN \_ GETDISPINFOA** (ANSI)<br/>           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**LVN \_ SETDISPINFO**](lvn-setdispinfo.md)
</dt> </dl>

 

 





