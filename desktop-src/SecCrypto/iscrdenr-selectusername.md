---
description: Zeigt eine Benutzeroberfläche auswählen an, sodass ein Benutzername ausgewählt werden kann.
ms.assetid: 0a02d9e5-b2cf-4818-a2e1-89e6019e53d4
title: ISCrdEnr::selectUserName-Methode
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
ms.openlocfilehash: b6414b78c07f9dff8761456f92b1088c5ed7eb6c23e7c7ed0eb2cd3980677dca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119409420"
---
# <a name="iscrdenrselectusername-method"></a>ISCrdEnr::selectUserName-Methode

Die **selectUserName-Methode** zeigt eine **Benutzeroberfläche auswählen** an, sodass ein Benutzername ausgewählt werden kann.

Der Benutzername gilt für den Benutzer, in dessen Namen die Zertifikatregistrierung vorgesehen ist.

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

*dwFlags* \[ In\]
</dt> <dd>

Für die zukünftige Verwendung reserviert. Legen Sie diesen Wert auf 0 (null) fest.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

### <a name="vb"></a>VB

Wenn die Methode erfolgreich ist, gibt die Methode S \_ OK zurück.

Wenn die Methode fehlschlägt, wird ein **HRESULT-Wert** zurückgegeben, der den Fehler angibt. Eine Liste der allgemeinen Fehlercodes finden Sie unter [Allgemeine HRESULT-Werte.](common-hresult-values.md)

## <a name="remarks"></a>Hinweise

Verwenden Sie diese Methode, um den Namen des Benutzers auszuwählen. Nachdem ein Benutzername ausgewählt wurde, kann sein Wert durch Aufrufen der [**ISCrdEnr::getUserName-Methode**](iscrdenr-getusername.md) abgerufen werden.

Eine Alternative zur Verwendung der Benutzeroberfläche "Benutzer auswählen" ist das Angeben eines Benutzers durch Aufrufen der [**ISCrdEnr::setUserName-Methode.**](iscrdenr-setusername.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Scrdenrl.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCrdEnr ist als 753988a1-1357-436d-9cf5-f089bdd67d64 definiert.<br/>             |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ISCrdEnr**](iscrdenr.md)
</dt> <dt>

[**ISCrdEnr::getUserName**](iscrdenr-getusername.md)
</dt> <dt>

[**ISCrdEnr::resetUser**](iscrdenr-resetuser.md)
</dt> <dt>

[**ISCrdEnr::setUserName**](iscrdenr-setusername.md)
</dt> </dl>

 

 




