---
description: Die Funktion "setPort" legt den einem Druckerport zugeordneten Status fest.
ms.assetid: 1b80ad93-aaa1-41ed-a668-a944fa62c3eb
title: SetPort-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetPort
- SetPortA
- SetPortW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: ab986128c9561b7b95de668367cafb0b3e6cd636
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042212"
---
# <a name="setport-function"></a>SetPort-Funktion

Die Funktion " **setPort** " legt den einem Druckerport zugeordneten Status fest.

## <a name="syntax"></a>Syntax


```C++
BOOL SetPort(
  _In_ LPTSTR pName,
  _In_ LPTSTR pPortName,
  _In_ DWORD  dwLevel,
  _In_ LPBYTE pPortInfo
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PName* \[ in\]
</dt> <dd>

Zeiger auf eine mit NULL endend beendete Zeichenfolge, die den Namen des Drucker Servers angibt, mit dem der Port verbunden ist. Legen Sie diesen Parameter auf **null** fest, wenn sich der Port auf dem lokalen Computer befindet.

</dd> <dt>

*pportname* \[ in\]
</dt> <dd>

Zeiger auf eine mit NULL endend beendete Zeichenfolge, die den Namen des Drucker Anschlusses angibt.

</dd> <dt>

*dwlevel* \[ in\]
</dt> <dd>

Gibt den Typ der Struktur an, auf die durch den *pportinfo* -Parameter verwiesen wird.

Dieser Wert muss 3 sein, was der Datenstruktur [**Port \_ Info \_ 3**](port-info-3.md) entspricht.

</dd> <dt>

*pportinfo* \[ in\]
</dt> <dd>

Ein Zeiger auf eine [**Port \_ Info \_ 3**](port-info-3.md) -Struktur, die die festzulegenden Port Statusinformationen enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein Wert ungleich 0 (null).

Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Dies ist eine blockierende oder synchrone Funktion, die möglicherweise nicht sofort zurückgegeben wird. Wie schnell diese Funktion zurückgibt, hängt von Lauf Zeitfaktoren ab, wie z. b. Netzwerkstatus, Druckserver Konfiguration und Implementierungs Faktoren für Druckertreiber, die beim Schreiben einer Anwendung schwierig vorhergesagt werden können. Wenn diese Funktion von einem Thread aufgerufen wird, der die Interaktion mit der Benutzeroberfläche verwaltet, könnte die Anwendung scheinbar nicht mehr reagiert.

 

Der Aufrufer der Funktion " **setPort** " muss als Administrator ausgeführt werden. Wenn es sich beim Aufrufer um einen Port Monitor oder einen sprach Monitor handelt, muss er außerdem [**revertyself**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-reverttoself) aufrufen, um den Identitätswechsel zu beenden, bevor **setPort** aufgerufen wird.

Alle Programme, die **setPort** aufrufen, müssen über Server \_ Zugriffsberechtigungen \_ für den Server verfügen, mit dem der Port verbunden ist.

Wenn Sie einen druckerportstatuswert mit dem Wert " \_ \_ Fehler beim Porttyp" festlegen \_ , beendet der Druck Spooler das Senden von Aufträgen an den Port. Der Druck Spooler setzt das Senden von Aufträgen an den Port fort, wenn der Port Status durch einen anderen Aufrufen von **setPort** gelöscht wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                      |
| Header<br/>                   | <dl> <dt>Winspool. h (Include Windows. h)</dt> </dl> |
| Bibliothek<br/>                  | <dl> <dt>Winspool. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool. drv</dt> </dl>                   |
| Unicode- und ANSI-Name<br/>   | **Setportw** (Unicode) und **setporta** (ANSI)<br/>                                                 |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Drucken](printdocs-printing.md)
</dt> <dt>

[Druckspooler-API-Funktionen](printing-and-print-spooler-functions.md)
</dt> <dt>

[**Port \_ Info \_ 3**](port-info-3.md)
</dt> </dl>

 

