---
description: Benachrichtigung, die an das Ansichts Rückruf Objekt gesendet wurde, um die Speicherorte und Ereignisse anzugeben, die für Änderungs Benachrichtigungs Ereignisse registriert werden sollen.
title: SFVM_GETNOTIFY Meldung (shlobj. h)
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
ms.openlocfilehash: f766ee74463dd820c0b55d501d5002a3378a97b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216832"
---
# <a name="sfvm_getnotify-message"></a>Sfvm \_ getnotify-Nachricht

Benachrichtigung, die an das Ansichts Rückruf Objekt gesendet wurde, um die Speicherorte und Ereignisse anzugeben, die für Änderungs Benachrichtigungs Ereignisse registriert werden sollen. Nachdem Sie registriert wurden, wird das View Callback-Objekt benachrichtigt, wenn eine Änderung in einer dieser Speicherorte oder Ereignisse auftritt. Diese Ereignisse werden über [**sfvm \_ fsnotify**](sfvm-fsnotify.md) an den Rückruf der Ansicht gesendet und dann von der-Sicht behandelt.


```C++
SFVM_GETNOTIFY 

    wParam = (WPARAM)(LPITEMIDLIST*) pidl;

    lParam = (LPARAM)(LONG*) lEvents;

            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PIDL* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine absolute idlist eines Elements, für das die Ansicht registriert werden soll, um über Änderungen benachrichtigt zu werden. In der Regel ist dies identisch mit der idlist des angezeigten Standorts, aber es kann sich um einen anderen Speicherort handeln.

> [!IMPORTANT]
> Die Lebensdauer dieses Werts liegt im Besitz des Ansichts Rückruf Objekts. Es liegt in der Verantwortung des Ansichts Rückruf Objekts, diesen Wert zu erstellen und freizugeben, wenn er nicht mehr benötigt wird. Dies erfordert, dass das Ansichts Rückruf Objekt diesen Wert speichert. Normalerweise kann der Wert im **\_ pidlmonitor** -Member des Ansichts Rückruf Objekts gespeichert werden. Die Besitz Regeln für den von *PIDL* zurückgegebenen Wert entsprechen nicht dem Standard und erfordern besondere Sorgfalt. Das Ansichts Rückruf Objekt muss diesen Wert besitzen und sicherstellen, dass es nicht freigegeben wird, bis das Ansichts Rückruf Objekt selbst zerstört wird.

 

</dd> <dt>

*levents* \[ vorgenommen\]
</dt> <dd>

Ein-Wert, der einen oder mehrere shcne-Werte enthält. Eine Liste möglicher Werte finden Sie unter [**shchangenotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) . Das View Callback-Objekt wird registriert, um eine [**sfvm- \_ fsnotify**](sfvm-fsnotify.md) -Nachricht zu empfangen, wenn eines der zugeordneten Ereignisse auftritt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wird ignoriert, sollte jedoch S \_ OK zurückgeben.

## <a name="remarks"></a>Bemerkungen

Wenn diese Rückruf Meldung weder für die idlist-noch für die Ereignis Maske einen Wert ungleich 0 (null) zurückgibt, wird die Ansicht nicht für Änderungs Benachrichtigungen registriert.

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt eine Beispiel Implementierung des Handlercodes der Ansichts Rückruffunktion für **sfvm \_ getnotify**.


```C++
case SFVM_GETNOTIFY:
  *((LPITEMIDLIST*)wParam) = _pidl;    // Pass a reference whose lifetime this 
                                       // class is responsible for.
                                      
  *((LONG*)lParam) = SHCNE_DISKEVENTS; // A combination of all of the 
                                       // disk event identifiers.
                                       
   return S_OK;
```



## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**sfvm \_ queryfsnotify**](sfvm-queryfsnotify.md)
</dt> <dt>

[**Ishellfolderviewcb:: messagesfvcb**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)
</dt> </dl>

 

 
