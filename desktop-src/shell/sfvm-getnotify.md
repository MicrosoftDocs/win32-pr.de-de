---
description: Benachrichtigung, die an das Ansichtsrückrufobjekt gesendet wird, um die Speicherorte und Ereignisse anzugeben, die für Änderungsbenachrichtigungsereignisse registriert werden sollen.
title: SFVM_GETNOTIFY Meldung (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 87933217-dfa9-4aaf-9630-fa2c302b18fa
api_name:
- SFVM_GETNOTIFY
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 04c96793e329bfc18c6e6f01b4112429d76b58eabdec276d500c36677e58245c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117677283"
---
# <a name="sfvm_getnotify-message"></a>SFVM \_ GETNOTIFY-Nachricht

Benachrichtigung, die an das Ansichtsrückrufobjekt gesendet wird, um die Speicherorte und Ereignisse anzugeben, die für Änderungsbenachrichtigungsereignisse registriert werden sollen. Sobald sie registriert sind, wird das Ansichtsrückrufobjekt benachrichtigt, wenn eine Änderung an diesen Speicherorten oder Ereignissen in auftritt. Diese Ereignisse werden über [**SFVM \_ FSNOTIFY**](sfvm-fsnotify.md) an den Ansichtsrückruf gesendet und dann von der Ansicht behandelt.


```C++
SFVM_GETNOTIFY 

    wParam = (WPARAM)(LPITEMIDLIST*) pidl;

    lParam = (LPARAM)(LONG*) lEvents;

            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pidl* \[ out\]
</dt> <dd>

Ein Zeiger auf eine absolute IDList eines Elements, für das die Sicht registriert werden soll, um über Änderungen benachrichtigt zu werden. In der Regel entspricht dies der IDList des angezeigten Standorts, kann aber ein anderer Speicherort sein.

> [!IMPORTANT]
> Die Lebensdauer dieses Werts befindet sich im Besitz des Ansichtsrückrufobjekts. Es liegt in der Verantwortung des Ansichtsrückrufobjekts, diesen Wert zu erstellen und dann frei zu machen, wenn er nicht mehr benötigt wird. Dies erfordert, dass das Ansichtsrückrufobjekt diesen Wert speichert. In der Regel kann der Wert im **\_ pidlMonitor-Member** des Ansichtsrückrufobjekts gespeichert werden. Die Besitzregeln für den von *pidl* zurückgegebenen Wert sind nicht dem Standard entsprechen und erfordern besondere Sorgfalt. Das Ansichtsrückrufobjekt muss diesen Wert besitzen und sicherstellen, dass er erst freigegeben wird, wenn das Ansichtsrückrufobjekt selbst zerstört wird.

 

</dd> <dt>

*lEvents* \[ out\]
</dt> <dd>

Ein -Wert, der mindestens einen SHCNE-Wert enthält. Eine Liste der möglichen Werte finden Sie unter [**SHChangeNotify.**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) Das Ansichtsrückrufobjekt wird registriert, um eine [**SFVM \_ FSNOTIFY-Nachricht**](sfvm-fsnotify.md) zu empfangen, wenn eines der zugeordneten Ereignisse auftritt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Ignoriert, sollte aber S \_ OK zurückgeben.

## <a name="remarks"></a>Hinweise

Wenn diese Rückrufmeldung weder für die IDList noch für die Ereignismaske einen Wert ungleich 0 (null) zurückgibt, wird die Sicht nicht für Änderungsbenachrichtigungen registriert.

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt eine Beispielimplementierungen des Handlercodes der Ansichtsrückruffunktion für **SFVM \_ GETNOTIFY.**


```C++
case SFVM_GETNOTIFY:
  *((LPITEMIDLIST*)wParam) = _pidl;    // Pass a reference whose lifetime this 
                                       // class is responsible for.
                                      
  *((LONG*)lParam) = SHCNE_DISKEVENTS; // A combination of all of the 
                                       // disk event identifiers.
                                       
   return S_OK;
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**SFVM \_ QUERYFSNOTIFY**](sfvm-queryfsnotify.md)
</dt> <dt>

[**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)
</dt> </dl>

 

 
