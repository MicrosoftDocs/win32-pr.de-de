---
description: Anlagen-Snap-in-Erweiterungen müssen die iscesvplattachmentpersistinfo-Schnittstelle implementieren.
ms.assetid: fadd2e06-d27c-4938-ad0e-ae7beab25931
title: Implementieren von iscesvplattachmentpersistinfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 941c86b1974b215c4353739f0514cb32bd6f239a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348751"
---
# <a name="implementing-iscesvcattachmentpersistinfo"></a><span data-ttu-id="5cef0-103">Implementieren von iscesvplattachmentpersistinfo</span><span class="sxs-lookup"><span data-stu-id="5cef0-103">Implementing ISceSvcAttachmentPersistInfo</span></span>

<span data-ttu-id="5cef0-104">Anlagen-Snap-in-Erweiterungen müssen die [**iscesvplattachmentpersistinfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo) -Schnittstelle implementieren.</span><span class="sxs-lookup"><span data-stu-id="5cef0-104">Attachment snap-in extensions must implement the [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo) interface.</span></span> <span data-ttu-id="5cef0-105">Mithilfe der Sicherheitskonfigurations-Snap-Ins wird diese Schnittstelle regelmäßig abgefragt, z. b. wenn die Konfiguration gespeichert oder das Snap-in geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="5cef0-105">The Security Configuration snap-ins query this interface periodically, such as when saving the configuration or closing the snap-in.</span></span> <span data-ttu-id="5cef0-106">Dadurch kann die Snap-in-Erweiterung alle Änderungen speichern, die der Benutzer möglicherweise an der Inspektions Datenbank oder der zugeordneten Konfiguration vorgenommen hat.</span><span class="sxs-lookup"><span data-stu-id="5cef0-106">This allows the snap-in extension to save any modifications that the user may have made to the inspection database or to the associated configuration.</span></span>

<span data-ttu-id="5cef0-107">Das folgende Beispiel zeigt eine Möglichkeit zum Implementieren von [**iscesvplattachmentpersistinfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo).</span><span class="sxs-lookup"><span data-stu-id="5cef0-107">The following example shows one way to implement [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo).</span></span>


```C++
#include <windows.h>

class CSceSvcAttachmentPersistInfo:
  public ISceSvcAttachmentPersistInfo,
  public CComObjectRoot
{
    BEGIN_COM_MAP(CSceSvcAttachmentPersistInfo)
    COM_INTERFACE_ENTRY(ISceSvcAttachmentPersistInfo)
    END_COM_MAP()

    friend class CDataObject;
    friend class CComponentDataImpl;

    CSceSvcAttachmentPersistInfo();
    ~CSceSvcAttachmentPersistInfo();

public:

    // ISceSvcAttachmentPersistInfo interface members
    STDMETHOD(IsDirty)(LPTSTR lpTemplateName);
    STDMETHOD(Save)(LPTSTR lpTemplateName, SCESVC_HANDLE *pscesvcHandle,
         PVOID *ppvData, PBOOL pbOverwriteAll );
    STDMETHOD(FreeBuffer)(PVOID pvData);

    //...

};

//
// Implementing IsDirty
//
STDMETHODIMP CSceSvcAttachmentPersistInfo::IsDirty(LPTSTR lpTemplateName)
{
  if ( m_pSnapin == NULL ) 
  {
    return S_FALSE;
  }
  //
  // just calling the snap-in's main IsDirty
  //
  return m_pSnapin->IsDirty();
}

//
// Implementing Save
//
STDMETHODIMP CSceSvcAttachmentPersistInfo::Save(LPTSTR lpTemplateName,
       SCE_HANDLE *psceHandle, 
       PVOID *ppvData, 
       PBOOL pbOverwriteAll )
{
  if ( psceHandle == NULL || ppvData == NULL || 
       pbOverwriteAll == NULL ) 
  {
    return E_INVALIDARG;
  }

  if ( m_pSnapin != NULL ) 
  {

    m_pSnapin->SaveDataInBuffer(lpTemplateName, psceHandle,
       ppvData, pbOverwriteAll);

    *psceHandle = m_sceHandle;

  }

  return S_OK;
}

//
// Implementing FreeBuffer
//
STDMETHODIMP CSceSvcAttachmentPersistInfo::FreeBuffer(PVOID pvData)
{
  if ( pvData == NULL ) 
  {
    return S_OK;
  }

  PSCESVC_ANALYSIS_INFO pTempInfo=(PSCESVC_ANALYSIS_INFO)pvData;

  if ( pTempInfo->Lines != NULL ) 
  {

    for ( DWORD i=0; i < pTempInfo->Count; i++ ) 
    {

      if ( pTempInfo->Lines[i].Key != NULL )
        LocalFree(pTempInfo->Lines[i].Key);

      if ( pTempInfo->Lines[i].Value != NULL )
        LocalFree(pTempInfo->Lines[i].Value);
    }

    LocalFree( pTempInfo->Lines);
  }

  LocalFree(pTempInfo);

  return S_OK;
}
```



 

 



