---
title: Iconfigasfwriter-Methode "konfigurifisingprofile"
description: Die Methode "Konfigurations Methode" ist die empfohlene Vorgehensweise zum Festlegen eines Profils. Er konfiguriert den Filter zum Schreiben einer ASF-Datei auf Grundlage des angegebenen Anwendungs definierten Profils.
ms.assetid: 278e5109-ba22-4a1c-9c6a-5cfcb9f57d37
keywords:
- Konfigurieren von Windows Media-Format für die Methode "Konfigurations Methode"
- Konfigurations Methode für das Windows Media-Format (Windows Media Format), iconfigasfwriter-Schnittstelle
- Iconfigasfwriter-Schnittstelle Windows Media-Format, Methode "konfigurifiterusingprofile"
topic_type:
- apiref
api_name:
- IConfigAsfWriter.ConfigureFilterUsingProfile
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 07b8d87fbf7e8b2d1d46acf55fe96bfdfef472b4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106338083"
---
# <a name="iconfigasfwriterconfigurefilterusingprofile-method"></a>Iconfigasfwriter:: konfiguriert refilterusingprofile-Methode

Die Methode " **Konfigurations** Methode" ist die empfohlene Vorgehensweise zum Festlegen eines Profils. Er konfiguriert den Filter zum Schreiben einer ASF-Datei auf Grundlage des angegebenen Anwendungs definierten Profils.

## <a name="syntax"></a>Syntax


```C++
HRESULT ConfigureFilterUsingProfile(
  [in] IWMProfile *pProfile
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pprofile* \[ in\]
</dt> <dd>

Zeiger auf die [**iwmprofile**](iwmprofile.md) -Schnittstelle im Anwendungs definierten Profil.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                                         | Beschreibung                                                   |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                | Die Methode wurde erfolgreich ausgeführt.<br/>                              |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>           | Der **iwmprofile** -Schnittstellen Zeiger ist ungültig.<br/> |
| <dl> <dt>**VFW \_ E \_ falscher \_ Zustand**</dt> </dl> | Das Diagramm wurde beendet.<br/>                              |



 

## <a name="remarks"></a>Bemerkungen

Bei erfolgreicher Ausführung bewirkt diese Methode, dass **ein \_ \_ geändertes Ereignis des EC-Diagramms** an die Anwendung gesendet wird. Verwenden Sie diese Methode, um den Writer mit einem benutzerdefinierten Windows Media 9-Serien Profil zu konfigurieren, das Sie mithilfe der Methoden des SDK für den Windows Media-Format erstellt (oder aus einer vorhandenen PRX-Datei geladen haben).

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iconfigasfwriter-Schnittstelle**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))
</dt> </dl>

 

