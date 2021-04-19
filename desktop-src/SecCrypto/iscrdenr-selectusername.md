---
description: Zeigt eine Benutzeroberfläche zum auswählen an, sodass ein Benutzername ausgewählt werden kann.
ms.assetid: 0a02d9e5-b2cf-4818-a2e1-89e6019e53d4
title: 'Iscrdenr:: selectusername-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.selectUserName
- SCrdEnr.selectUserName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 13059775abc8520c39a0ad3dea2d604fc8d65455
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353887"
---
# <a name="iscrdenrselectusername-method"></a>Iscrdenr:: selectusername-Methode

Die **selectusername** -Methode zeigt eine Benutzeroberfläche zum **auswählen** an, sodass ein Benutzername ausgewählt werden kann.

Der Benutzername gilt für den Benutzer, für den die Zertifikat Registrierung vorgesehen ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT selectUserName(
  [in] DWORD dwFlags
);
```


```VB

SCrdEnr.selectUserName( _
  ByVal dwFlags _
)
```





## <a name="parameters"></a>Parameter

<dl> <dt>

*dwFlags* \[ in\]
</dt> <dd>

Für die zukünftige Verwendung reserviert. Legen Sie diesen Wert auf NULL fest.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

### <a name="vb"></a>VB

Wenn die Methode erfolgreich ausgeführt wird, gibt die Methode S \_ OK zurück.

Wenn die Methode fehlschlägt, wird ein **HRESULT** -Wert zurückgegeben, der den Fehler angibt. Eine Liste der allgemeinen Fehlercodes finden Sie unter [Allgemeine HRESULT-Werte](common-hresult-values.md).

## <a name="remarks"></a>Bemerkungen

Verwenden Sie diese Methode, um den Namen des Benutzers auszuwählen. Nachdem ein Benutzername ausgewählt wurde, kann der zugehörige Wert durch Aufrufen der [**iscrdenr:: GetUserName**](iscrdenr-getusername.md) -Methode abgerufen werden.

Eine Alternative zum Verwenden der Benutzeroberfläche "Select User" ist das Angeben eines Benutzers durch Aufrufen der [**iscrdenr:: setUserName**](iscrdenr-setusername.md) -Methode.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Scrdenrl.dll</dt> </dl> |
| IID<br/>                      | IID \_ iscrdenr ist definiert als 753988a1-1357-436d-9cf5-f089bdd67d64<br/>             |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iscrdenr**](iscrdenr.md)
</dt> <dt>

[**Iscrdenr:: GetUserName**](iscrdenr-getusername.md)
</dt> <dt>

[**Iscrdenr:: resetuser**](iscrdenr-resetuser.md)
</dt> <dt>

[**Iscrdenr:: setUserName**](iscrdenr-setusername.md)
</dt> </dl>

 

 




