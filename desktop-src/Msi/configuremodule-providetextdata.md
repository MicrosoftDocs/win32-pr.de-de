---
description: Die ProvideTextData-Methode wird von Mergemod.dll aufgerufen, um Textdaten aus dem Clienttool abzurufen. Mergemod.dll stellt den Namen aus dem entsprechenden Eintrag in der Tabelle ModuleConfiguration bereit.
ms.assetid: 286b0b58-1b6a-4d41-89e1-eb9c23bdd788
title: ConfigureModule.ProvideTextData-Methode (Mergemod.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfigureModule
- IMsmConfigureModule
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 9712b7e7f619e40ba3804d7c5671c6855e7982eddd2c4c964f172845cf5de465
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118143716"
---
# <a name="configuremoduleprovidetextdata-method"></a>ConfigureModule.ProvideTextData-Methode

Die **ProvideTextData-Methode** wird von Mergemod.dll aufgerufen, um Textdaten aus dem Clienttool abzurufen. Mergemod.dll stellt den *Namen* aus dem entsprechenden Eintrag in der Tabelle ModuleConfiguration bereit.

Das Tool sollte S OK zurückgeben \_ und den entsprechenden Anpassungstext in ConfigData bereitstellen. Das Clienttool ist für die Zuordnung der Daten zuständig, aber Mergemod.dllist für die Freigabe des Arbeitsspeichers verantwortlich. Dieses Argument MUSS ein **BSTR-Objekt** sein. **LPCWSTR** wird NICHT akzeptiert.

Wenn das Tool keine Konfigurationsdaten für diesen *Name-Wert* bereitstellt, sollte die Funktion S \_ FALSE zurückgeben. In diesem Fall ignoriert Mergemod.dll den Wert des ConfigData-Arguments und verwendet den Standardwert aus der Tabelle ModuleConfiguration.

Jeder andere Rückgabecode als S \_ OK oder S FALSE führt \_ dazu, dass ein Fehler protokolliert wird (wenn ein Protokoll geöffnet ist). Dies führt zu einem Fehler bei der Zusammenführung.

Da diese Funktion der **BSTR-Standardkonvention** entspricht, entspricht NULL der leeren Zeichenfolge.

## <a name="syntax"></a>Syntax


```JScript
ConfigureModule.ProvideTextData(
  Name,
  ConfigData
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Name* 
</dt> <dd>

Name des Elements, für das Daten abgerufen werden.

</dd> <dt>

*ConfigData* 
</dt> <dd>

Zeiger auf Anpassungstext.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Der Client kann nicht mehr als einmal für jeden Datensatz in der [Tabelle ModuleConfiguration](moduleconfiguration-table.md)aufgerufen werden. Beachten Sie, dass Mergemod.dll nie mehrere Aufrufe an den Client für denselben "Name"-Wert vornimmt. Wenn kein Datensatz in der Tabelle ModuleSubsschädigung die -Eigenschaft verwendet, verursacht ein Eintrag in der Tabelle ModuleConfiguration keine Aufrufe an den Client.

### <a name="c"></a>C++

Siehe [**ProvideTextData-Funktion.**](/windows/desktop/api/Mergemod/nf-mergemod-imsmconfiguremodule-providetextdata)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Mergemod.dll 2.0 oder höher<br/>                                                    |
| Header<br/>  | <dl> <dt>Mergemod.h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




